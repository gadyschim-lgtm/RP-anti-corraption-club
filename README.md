# RP Anti-Corruption Club

## 🌍 About the Project

**RP Anti-Corruption Club** is a modern, responsive, and privacy-focused digital platform designed to support awareness, reporting, and communication related to corruption, injustice, and unethical practices.

The platform is designed for use on:

- 📱 Mobile phones
- 💻 Laptops
- 🖥️ Desktop computers
- 🌐 Modern web browsers

The system provides both **private reporting** and **public awareness** features while protecting the identity of users in the public area.

---

# 🎯 Project Objectives

The main objectives of RP Anti-Corruption Club are to:

1. Provide a secure way for users to report suspected corruption or injustice.
2. Allow users to communicate privately with administrators.
3. Provide a public platform for anti-corruption awareness.
4. Protect the identity of users in public posts.
5. Allow users to submit evidence such as files, voice notes, and video notes.
6. Provide secure user authentication.
7. Provide administrators with tools to manage reports and messages.
8. Support QR code scanning.
9. Provide a responsive experience on different devices.
10. Promote transparency, accountability, and responsible reporting.

---

# ✨ Main Features

## 🔐 1. User Authentication

Users can create an account and sign in using:

- Registration Number
- Password
- Retype Password during registration

The system also provides:

- Sign In
- Sign Up
- Forgot Password
- Sign Out

### Registration

A user provides:

- Registration Number
- Password
- Retype Password

The password must meet the minimum security requirements configured by the application.

---

# 🔑 2. Forgot Password

The platform includes a password recovery feature.

The system should verify the registration number securely before allowing password recovery.

For a production deployment, password-reset verification should be performed server-side rather than exposing account information directly in browser JavaScript.

---

# 🚨 3. Private Reporting System

Users can submit private reports to administrators.

A report can contain:

- Subject
- Written description
- Voice note
- Video note
- Supporting files

Examples of reports include:

- Suspected corruption
- Abuse of authority
- Unfair treatment
- Misuse of resources
- Fraud
- Bribery
- Other forms of injustice

Private reports are intended to be accessible only to the reporting user and authorized administrators.

---

# 💬 4. Private Communication

After submitting a report, the user can communicate privately with an administrator.

The system supports a private conversation such as:

**User → Admin**

and

**Admin → User**

This allows administrators to:

- Read reports
- Ask questions
- Request additional evidence
- Respond to the user
- Follow up on a case

Other users must not have access to these private conversations.

---

# 🎙️ 5. Voice Notes

Users can record a voice message directly from their device.

The application uses browser media permissions to access the microphone.

Voice notes can be used when a user prefers speaking instead of typing.

---

# 🎥 6. Video Notes

Users can record a video note using their device camera.

This can be useful when visual information is important to a report.

The browser will request permission to access:

- Camera
- Microphone

---

# 📁 7. File Upload

Users can attach supporting evidence from their own device.

Examples include:

- Images
- Documents
- PDFs
- Other permitted file types

File uploads should be restricted using:

- File-size limits
- Allowed MIME types
- File-extension validation
- Secure storage
- Malware scanning where available

---

# 📢 8. Public Awareness Posts

Users can create public awareness posts.

Public posts may contain:

- Title
- Text
- Images or other permitted media

Public posts are visible to the community.

---

# 🤖 9. Anonymous Public Identity

The public feed does **not** display the author's personal profile.

Instead, posts use an anonymous identity such as:

> 🤖 Anonymous Community Robot

The purpose is to reduce unnecessary exposure of user identity.

Users should not be able to open another user's profile from public posts.

---

# ❤️ 10. Likes

Public posts can receive likes.

The platform can record:

- Number of likes
- Whether the current user has liked a post

Users can like or unlike public posts.

---

# 👁️ 11. Views

Public posts can display the number of views.

The system can record when content is viewed and update the view counter.

---

# 📱 12. QR Code Scanner

The platform includes QR code scanning functionality.

Users can scan QR codes using the device camera.

Possible future uses include:

- Opening official information
- Accessing campaigns
- Joining awareness activities
- Verifying information
- Opening specific platform resources

Camera permission is required for QR scanning.

---

# ⚙️ 13. User Settings

Users have access to their own settings.

The system should allow users to manage appropriate account preferences.

Users should **not** be able to browse or edit other users' profiles.

---

# 👨‍💼 14. Administrator System

Administrators have additional functionality that ordinary users do not have.

The administrator can:

- View private reports
- Read private messages
- Reply to users
- Review submitted evidence
- Manage public posts
- Manage platform content
- Monitor platform activity
- Perform administrative actions

Administrator privileges must be enforced on the server/database side.

---

# 🔒 Privacy and Security

Privacy is one of the most important parts of this project.

Private reports may contain sensitive information. Therefore, the production system should use strong security controls.

Recommended security features include:

- HTTPS
- Secure authentication
- Database Row Level Security (RLS)
- Private storage buckets
- Strong administrator authentication
- Multi-factor authentication (MFA)
- Rate limiting
- Input validation
- File validation
- Malware scanning
- Audit logs
- Secure password recovery
- Short-lived private file URLs
- Minimal collection of personal information
- Regular backups
- Security monitoring

---

# ⚠️ Important Security Limitation

A website made only with HTML, CSS, and JavaScript cannot guarantee that users will be unable to:

- Take screenshots
- Record their screen
- Copy information using another device
- Capture content using operating-system tools

Browser JavaScript can discourage some actions, but it cannot provide complete protection against operating-system-level screenshots or screen recording.

For sensitive content, additional protections should be used, such as:

- Watermarking
- Access control
- Private storage
- Expiring URLs
- Server-side authorization
- Audit logging

The system should never be described as completely "hack-proof."

---

# 🏗️ Technology Stack

The frontend can be built using:

### HTML5

Used for the application structure.

### CSS

Used for styling and responsive layouts.

### JavaScript

Used for:

- Authentication logic
- User interactions
- Recording
- File handling
- QR scanning
- API communication
- Dynamic content

### Tailwind CSS

Used for responsive and modern UI design.

### Font Awesome

Used for application icons.

### Supabase

Supabase can provide:

- Authentication
- PostgreSQL database
- Storage
- Row Level Security
- Backend services

### QR Code Library

A browser-compatible QR code library can be used to scan QR codes using the device camera.

---

# 🗄️ Suggested Database Structure

A production version can use tables such as:

```text
profiles
private_reports
private_messages
posts
post_likes
post_views
audit_logs
