# CS 305: Software Security
## Portfolio Reflection — Artemis Financial

### Project Overview

Throughout CS 305, I worked as a software developer for Global Rain, a software engineering company tasked with improving the security of Artemis Financial's web application. Artemis Financial provides individualized financial planning services, including savings, retirement, investments, and insurance. Because the company handles sensitive customer and financial information, maintaining secure communications and protecting data integrity were essential priorities.

The primary objective was to identify potential vulnerabilities within the existing application and implement security enhancements. These improvements included establishing secure HTTPS communications, generating a self-signed security certificate, implementing a SHA-256 checksum verification mechanism, and conducting dependency vulnerability assessments.

### Identifying Security Vulnerabilities and the Importance of Secure Coding

One aspect of this project that I believe I handled particularly well was approaching security as an ongoing process rather than a single implementation. Instead of assuming that adding encryption and checksum verification would make the application secure, I evaluated the application's dependencies and tested the effectiveness of the changes.

Secure coding is especially important for organizations such as Artemis Financial because vulnerabilities can expose sensitive financial information, compromise customer privacy, and damage an organization's reputation. Implementing secure coding practices helps protect data confidentiality and integrity, supports regulatory compliance, and strengthens customer confidence.

### Challenges and Lessons Learned

The most challenging and educational portion of this project involved using OWASP Dependency-Check to identify and evaluate security vulnerabilities.

My initial assessment identified 151 reported vulnerability findings across seven dependencies. After updating Spring Boot and its associated dependencies, I reduced the reported findings to 61 across five dependencies.

However, resolving the Maven build failures required additional troubleshooting. I encountered issues involving dependency compatibility, Java application execution, vulnerability severity thresholds, and authentication errors from the Sonatype OSS Index analyzer.

Working through these challenges helped me better understand how security testing tools operate and the importance of distinguishing application functionality from dependency security. I also learned that a successful build does not necessarily mean an application is free of vulnerabilities.

### Implementing Layers of Security

I increased the application's security by implementing multiple protective measures.

First, I configured the application to use HTTPS rather than HTTP, providing encrypted communication through TLS. I generated a self-signed certificate using Java Keytool and configured the application to operate on port 8443.

Next, I implemented SHA-256 hashing to generate a checksum for a unique verification string. This provided a mechanism for checking data integrity by comparing calculated hash values.

Finally, I used OWASP Dependency-Check to examine third-party libraries for known vulnerabilities and updated dependencies to reduce the number of reported findings.

In future projects, I would continue using vulnerability scanners, manual code reviews, and dependency analysis to evaluate potential security risks. I would also consider vulnerability severity, exploitability, application configuration, and available security patches when selecting mitigation strategies.

### Functional Testing and Security Verification

To verify that the refactored application remained functional, I compiled and executed the Java application using Eclipse and Maven. I confirmed that the Spring Boot server started successfully and that the HTTPS endpoint displayed the expected SHA-256 checksum and personalized verification data.

I also performed secondary vulnerability testing using OWASP Dependency-Check after updating the application's dependencies.

The initial scan reported 151 vulnerability findings, while the later scan reported 61. This comparison demonstrated that the dependency updates reduced the number of reported findings, although additional vulnerabilities remained.

To resolve build interruptions, I adjusted the OWASP vulnerability failure threshold and disabled the OSS Index analyzer after encountering authentication errors. These changes allowed the build to complete but did not eliminate the remaining security findings. This experience reinforced the importance of accurately interpreting security testing results.

### Tools, Resources, and Secure Coding Practices

Several tools and techniques used throughout this project will be valuable in future software development assignments and professional work.

Eclipse provided the development environment for implementing and testing Java code, while Maven supported dependency management and application builds. Java Keytool allowed me to generate and export a self-signed certificate, and Spring Boot provided the framework for configuring HTTPS communication.

OWASP Dependency-Check was particularly valuable because it demonstrated how third-party dependencies can introduce security risks even when the application's custom code functions correctly.

I also gained experience implementing SHA-256 hashing, configuring TLS, troubleshooting Maven dependencies, and interpreting vulnerability reports.

These tools and practices will help me develop software that is more secure, maintainable, and adaptable.

### Demonstrating My Skills to Future Employers

I would include my completed Artemis Financial Practices for Secure Software Report in my professional portfolio because it demonstrates both technical knowledge and practical problem-solving.

The project provides evidence of my ability to evaluate security vulnerabilities, implement secure communication protocols, configure cryptographic functionality, and conduct security testing.

I believe the most valuable aspect of this project is that it demonstrates my ability to work through unexpected technical challenges. Rather than simply implementing code, I investigated errors, evaluated vulnerability findings, updated dependencies, and verified that the application continued functioning after changes.

This experience strengthened my understanding that secure software development requires continuous assessment, careful documentation, and a willingness to adapt as new security risks emerge.# CS-305-Portfolio
