# Recover password

**Functional Requeriments**

- The user can be able to recover your password with your e-mail;
- The user can be able to receive a e-mail with the instructions of your recover password;
- The user can be able to reset your password;

**Non-functional Requirements**

- Use Mailtrap to test sendings in dev enviroment;
- Use Amazon SES to sendings in production enviroment;
- The send of e-mails has to occur in second plan (background job);

**Business Rules**

- The link sent by e-mail to reset password, has be expired in 2h;
- The user needs to confirm the new password when resets your password;

# Update profile

**Functional Requeriments**

- The user can be able to update your name, email and password;

**Business Rules**

- The user can't be able to change your email for another in use;
- For update the password, the user has to inform your old password;
- For update the password, the user needs to confirm the new password;

# Provider dashboard

**Functional Requeriments**

- The user can be able to list your appointments in specific day;
- The provider has to receive a notification whenever there is a new appointment;
- The provider can be able to view unread notifications;

**Non-functional Requirements**

- Provider appointments for the day must be cached;
- The provider notifications must be stored in MongoDB;
- The provider notifications must be sent in real-time using Socket.io;

**Business Rules**

- The notifications must have a read or unread status so that the provider can control;

# Service appointments

**Functional Requeriments**

- The user can be able to list all the registered service providers;
- The user can be able to list the days of month with at least one time available from one provider;
- The user can be able to list availables times in a specific day from one provider;
- The user can be able to realize a new appointment with one provider;

**Non-functional Requirements**

- The list of providers has to be armazened in cache;

**Business Rules**

- Each appointment must last 1 hour;
- The appointments has to be available between 8h to 18h (First at 8h, last one to 17h);
- The user cannot be scheduled at unavaible time;
- The user cannot scheduled at a time that has already passed;
- The user cannot scheduled service with yourself;
