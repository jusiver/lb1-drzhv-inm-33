
### Installation
1. Download or clone the project repository to your local machine using `git clone https://github.com/jusiver/lb1-drzhv-inm-33.git .` (where `.` will be your current folder).
2. Open a command shell from the root folder of the project.
3. Run the following command to generate an SQLite database in the project folder: `make migrate`
4. Build the project by running the following command: `make`

### Configuration
To configure the web application, edit the parameter values in a .properties file. By default, the file is called `application.properties` if you use the make tool. Otherwise, you can name it anything and specify it as a call argument. You can also use environment variables. The settings of the application's aspects, including the embedded Jetty web server properties, mailing configuration, security strength, and database connection details, are determined by their usage. The project repository has [a file with default values set](application.properties), which you can use. For more flexibility, refer to the table below.

|Key|Value|
|---|---|
|application.host|The IP address to which the application should bind|
|application.port|The port on which the application should run|
|application.bcryptStrength|The strength of the bcrypt encryption algorithm|
|database.filename|The path to the SQLite database in either absolute or relative form|
|mail.from|The email address of the sender of the email|
|mail.user|The identifier of the sender of the email on SMTP server|
|mail.password|The credential that is used to authenticate the email sender on SMTP server|
|mail.host|The IP address to which the SMTP server should bind|
|mail.port|The port on which the SMTP server should run|
|mail.ssl|Determines whether to use SSL encryption or not|
|mail.auth|Determines whether or not the email sender should be authenticated on the SMTP server|

### Run
1. If you prefer to use a local SMTP server, run MailHog. Note that the default host is set to 0.0.0.0, which means "localhost" in the context of this program. The default ports are 1025 for SMTP connections and 8025 for HTTP connections, which provide a useful web interface for email management.
2. Start the application by running the following command from the command shell: `make run`
