# ***OAuth2 Authentication with Spring Security***

This guide will walk you through setting up OAuth2 authentication with Google using Spring Security in your Java application. OAuth2 is an industry-standard protocol for authorization, providing a secure and standardized way to access user data.

## Prerequisites:
Basic knowledge of Spring Boot and Spring Security.
A GitHub account to create OAuth2 credentials.
A Google account to create OAuth2 credentials.
JDK installed on your machine.
Maven or Gradle installed for dependency management.

## Steps to follow:

### Step 1: Create OAuth2 Credentials on Google (or Github) Developers Console
Navigate to the Google Developers Console.
Create a new project or select an existing one.
In the left sidebar, navigate to "Credentials" under "APIs & Services".
Click on "Create credentials" and select "OAuth client ID".
Choose the application type as "Web application".
Add "http://localhost:1234/login/oauth2/code/google" as an authorized redirect URI.
Click "Create" to generate your OAuth2 credentials (Client ID and Client Secret)

### Step 2: Configure Spring Security
Add the 'spring-boot-starter-oauth2-client' dependencies to your pom.xml or build.gradle file.

### Step 3: Configure OAuth2 properties in application.properties or application.yml.
Github Login:
spring.security.oauth2.client.registration.github.client-id= ${githubClientId}
spring.security.oauth2.client.registration.github.client-secret= ${githubSecret}

Google Login:
spring.security.oauth2.client.registration.google.client-id= ${googleClientId} 
spring.security.oauth2.client.registration.google.client-secret= ${googleSecret}

### Step 4: Configure Spring Security
Enable OAuth2 login in your Spring Security configuration.

### Step 5: Run Your Application
Start your Spring Boot application.
Navigate to the login page (/login).
Click on the "Login with Google" button.
You'll be redirected to Google's authentication page where you can sign in with your Google account.
After successful authentication, you'll be redirected back to your application.
Conclusion
Congratulations! You've successfully implemented OAuth2 authentication with Google using Spring Security in your application. Users can now log in securely using their Google accounts.

For more information on Spring Security and OAuth2, refer to the official documentation.

