---
name: Bug Report
about: Create a report to help us improve and fix a bug.
title: '[BUG] User profile image fails to upload with "File too large" error for 1.5MB image'
labels: bug, ui, backend
assignees: 'alice-dev'

---

**Describe the Bug**
When trying to upload a profile picture that is 1.5MB, the system shows a generic "File too large" error. The project documentation states the limit is 2MB.

**To Reproduce**
1. Log in as any user.
2. Navigate to 'My Profile' -> 'Edit Profile'.
3. Click the 'Change Avatar' button.
4. Select a JPEG image file that is 1.5MB in size.
5. Click 'Upload'.
6. See the red error banner: "Error: File too large."

**Expected Behavior**
The 1.5MB image should upload successfully, or the error message should clearly state the actual file size limit.

**Screenshots/Logs**
![Screenshot of the error message](link-to-screenshot.png)

**Environment (please complete the following information):**
 - OS: macOS Ventura 13.5
 - Browser: Chrome 119.0.6045.123
 - Version: Commit `f4e4c4d` (latest on `develop` branch)

**Additional Context**
- This also happens with 1.8MB PNG files.
- The issue does not occur with images under 1MB.
- I checked the network tab, and the API is returning a `413 Payload Too Large` status code.
