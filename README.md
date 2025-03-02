# Email Notification Templates

## 1. Login Notification

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">New Login Detected</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        We detected a recent login to your account from:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <p style="color:#555; line-height:1.6;">
        If this was you, no action is needed. If you don't recognize this activity, please secure your account immediately.
    </p>
    <div style="text-align:center; margin:25px 0;">
        <a href="/account/security" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Review Account Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Not you?</strong> Please <a href="/reset-password" style="color:#d32f2f; text-decoration:underline;">reset your password</a> and <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 2. Password Reset

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Password Reset Request</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        We received a request to reset your password. Use the button below to set a new password:
    </p>
    <div style="text-align:center; margin:25px 0;">
        <a href="${resetLink}" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Reset Password</a>
    </div>
    <p style="color:#555; line-height:1.6;">
        This link will expire in 30 minutes for your security.
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Request from:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Didn't request this?</strong> If you didn't request a password reset, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 3. OTP Verification

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Your Verification Code</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Your verification code is:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0; text-align:center;">
        <p style="color:#333; font-size:24px; letter-spacing:5px; font-weight:bold; margin:0;">
            ${otpCode}
        </p>
    </div>
    <p style="color:#555; line-height:1.6;">
        This code will expire in 10 minutes. Please do not share this code with anyone.
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Request from:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Didn't request this?</strong> If you didn't request this code, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 4. Account Verification

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Verify Your Account</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Thank you for signing up! Please verify your account to get started:
    </p>
    <div style="text-align:center; margin:25px 0;">
        <a href="${verificationLink}" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Verify My Account</a>
    </div>
    <p style="color:#555; line-height:1.6;">
        Or copy and paste this link into your browser:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0; word-break:break-all;">
        <p style="color:#555; line-height:1.6; margin:0; font-size:14px;">
            ${verificationLink}
        </p>
    </div>
    <p style="color:#555; line-height:1.6;">
        This link will expire in 24 hours.
    </p>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated message. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 5. Password Changed Confirmation

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Password Successfully Changed</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Your password was successfully changed. Here's a summary of this change:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:25px 0;">
        <a href="/account/security" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Review Account Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Wasn't you?</strong> If you didn't change your password, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 6. Email Update Confirmation

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Email Address Updated</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Your email address has been successfully updated. Here's a summary of this change:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Previous email:</strong> ${oldEmail}<br>
            <strong>New email:</strong> ${newEmail}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:25px 0;">
        <a href="/account/security" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Review Account Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Wasn't you?</strong> If you didn't change your email, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 7. Two-Factor Authentication

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">2FA Status Changed</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Two-factor authentication for your account has been ${status === 'enabled' ? 'enabled' : 'disabled'}. Here's a summary of this change:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Status:</strong> ${status === 'enabled' ? 'Enabled' : 'Disabled'}<br>
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:25px 0;">
        <a href="/account/security" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Review Account Security</a>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Wasn't you?</strong> If you didn't make this change, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 8. Payment Receipt

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Payment Receipt</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        Thank you for your payment. Here's a summary of your transaction:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Transaction ID:</strong> ${transactionId}<br>
            <strong>Date:</strong> ${new Date().toGMTString()}<br>
            <strong>Amount:</strong> ${amount}<br>
            <strong>Payment Method:</strong> ${paymentMethod}
        </p>
    </div>
    <table style="width:100%; border-collapse:collapse; margin:20px 0;">
        <thead>
            <tr style="background:#f8f9fa;">
                <th style="padding:10px; text-align:left; border-bottom:1px solid #eee;">Item</th>
                <th style="padding:10px; text-align:right; border-bottom:1px solid #eee;">Amount</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td style="padding:10px; text-align:left; border-bottom:1px solid #eee;">${itemName}</td>
                <td style="padding:10px; text-align:right; border-bottom:1px solid #eee;">${itemPrice}</td>
            </tr>
            <tr>
                <td style="padding:10px; text-align:left; border-bottom:1px solid #eee;"><strong>Total</strong></td>
                <td style="padding:10px; text-align:right; border-bottom:1px solid #eee;"><strong>${amount}</strong></td>
            </tr>
        </tbody>
    </table>
    <div style="text-align:center; margin:25px 0;">
        <a href="/account/billing" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">View Billing History</a>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated payment receipt. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 9. Account Deletion Confirmation

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Account Deletion Confirmation</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        We're sorry to see you go. Your account deletion request has been processed:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Account:</strong> ${userData.email}<br>
            <strong>Deletion requested:</strong> ${new Date().toGMTString()}<br>
            <strong>Data removal:</strong> Will be completed within 30 days
        </p>
    </div>
    <p style="color:#555; line-height:1.6;">
        All your personal data will be permanently deleted from our systems in accordance with our Privacy Policy.
    </p>
    <div style="text-align:center; margin:25px 0;">
        <a href="/reactivate?token=${reactivationToken}" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Reactivate My Account</a>
    </div>
    <p style="color:#555; line-height:1.6;">
        You can reactivate your account within the next 30 days by clicking the button above.
    </p>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Wasn't you?</strong> If you didn't request account deletion, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated notification. Please do not reply to this email.</p>
        <p>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 10. Event Reminder

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">Event Reminder</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        This is a reminder about your upcoming event:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>Event:</strong> ${eventName}<br>
            <strong>Date:</strong> ${eventDate}<br>
            <strong>Time:</strong> ${eventTime}<br>
            <strong>Location:</strong> ${eventLocation}
        </p>
    </div>
    <div style="text-align:center; margin:25px 0;">
        <a href="/calendar/event/${eventId}" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">View Event Details</a>
    </div>
    <p style="color:#555; line-height:1.6;">
        We're looking forward to seeing you there!
    </p>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated reminder. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 11. API Key Notification

```html
<div style="max-width:600px; margin:20px auto; font-family:Arial, sans-serif; padding:20px; border:1px solid #eee; border-radius:8px; box-shadow:0 2px 10px rgba(0,0,0,0.05);">
    <h2 style="color:#333; margin-top:0;">API Key ${action} Notification</h2>
    <p style="color:#555; line-height:1.6;">
        Hi ${userData.fullName},
    </p>
    <p style="color:#555; line-height:1.6;">
        We're notifying you that an API key for your account has been ${action}:
    </p>
    <div style="background:#f8f9fa; padding:15px; border-radius:5px; margin:15px 0;">
        <p style="color:#555; line-height:1.6; margin:0;">
            <strong>API Key Name:</strong> ${keyName}<br>
            <strong>Action:</strong> ${action}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}<br>
            <strong>IP Address:</strong> ${ipAddress}
        </p>
    </div>
    <div style="text-align:center; margin:25px 0;">
        <a href="/developer/api-keys" style="display:inline-block; padding:12px 24px; background:#0066cc; color:white; text-decoration:none; border-radius:4px; font-weight:bold;">Manage API Keys</a>
    </div>
    <div style="background:#fff8f8; border-left:4px solid #ff3b30; padding:12px; margin:20px 0;">
        <p style="color:#d32f2f; margin:0; font-size:14px;">
            <strong>Wasn't you?</strong> If you didn't make this change, please <a href="/support" style="color:#d32f2f; text-decoration:underline;">contact support</a> immediately.
        </p>
    </div>
    <div style="color:#999; font-size:12px; text-align:center; border-top:1px solid #eee; padding-top:15px; margin-top:30px;">
        <p style="margin-bottom:10px;">This is an automated security notification. Please do not reply to this email.</p>
        <p>
            <a href="/account/preferences" style="color:#777; text-decoration:none; margin:0 8px;">Email Preferences</a>
            <a href="/privacy" style="color:#777; text-decoration:none; margin:0 8px;">Privacy Policy</a>
            <a href="/help" style="color:#777; text-decoration:none; margin:0 8px;">Help Center</a>
        </p>
        <p style="margin-top:15px;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```
