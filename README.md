# Phone Sync (for Nextcloud & ownCloud)

Phone Sync provides a webinterface to display your SMS conversations. SMS conversations are pushed by your Android devices using the [Android client](https://github.com/nerzhul/ownCloud-SMS-App), available on [F-Droid](https://f-droid.org/repository/browse/?fdid=fr.unix_experience.owncloud_sms).

## :arrow_forward: Access

The app is available on the [Nextcloud App Store](https://apps.nextcloud.com/apps/ocsms), so installing is as easy as:

1. Navigate in your Nextcloud instance to the "Apps" 
2. Select the category "Multimedia"
3. Click "activate"

## :question: Solve encoding errors on MySQL
If you are on MySQL or MariaDB and have the following issue with the database:

```
Incorrect string value: '\xF0\x9F\x98\x89' for column 'sms_msg' at row 1
```

The cause may be that you have to enable 4-byte support. 

Here is a guide: https://docs.nextcloud.com/server/11/admin_manual/maintenance/mysql_4byte_support.html

## :question: Solve InnoDB 'Index column size too large' error on MySQL

If you are on MySQL or MariaDB and have the following issue with the database:

```
Index column size too large. The maximum column size is 767 bytes.
```

You should reconfigure your MySQL server to support a such column size.

Here are some informations: https://stackoverflow.com/questions/30761867/mysql-error-the-maximum-column-size-is-767-bytes/30767600

## :question: Solve the synchronisation issues
If you are using FastCGI you must enable buffering in FastCGI but commenting the following line:

```
fastcgi_request_buffering off;
```

## :question: Using the Android App With 2FA Enabled
If you've enabled 2FA (Two Factor Authentication) logins you may be hit with an incorrect password error. The android client doesn't support logging in with 2FA credentials. Here is a guide to do so, although it says Managing Devices it is the same process for App Passwords: https://docs.nextcloud.com/server/11/user_manual/session_management.html#managing-devices

## :eyes: Screenshot

![Screenshot](https://raw.githubusercontent.com/nextcloud/ocsms/master/appinfo/screenshots/1.png)

## :link: Requirements
- A [Nextcloud](https://nextcloud.com) or [ownCloud](https://owncloud.com) instance
- An Android phone

## :exclamation: Reporting issues

- **Server:** https://github.com/nextcloud/ocsms/issues
- **Client:** https://github.com/nerzhul/ownCloud-SMS-App/issues

## :notebook: License
Phone Sync web application is currently licensed under [AGPL license](https://github.com/nextcloud/ocsms/blob/master/LICENSE.md).

## :notebook: External Libraries
[Twemoji](https://github.com/twitter/twemoji) Code licensed under the [MIT License](http://opensource.org/licenses/MIT), Graphics licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).
[libphonenumber-for-php](https://github.com/giggsey/libphonenumber-for-php) Code licensed under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).
