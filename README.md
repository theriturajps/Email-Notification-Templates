# Email Notification Templates

## 1. Login Notification

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">New Login Detected</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">We detected a login from:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">If this was you, no action needed. Otherwise, secure your account now.</p>
    <div style="text-align:center; margin:15px 0;">
        <a href="/account/security" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Review Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Not you?</strong> <a href="/reset-password" style="color:#d32f2f;">Reset password</a> and <a href="/support" style="color:#d32f2f;">contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 2. Password Reset

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Password Reset Request</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Use the button below to set a new password:</p>
    <div style="text-align:center; margin:15px 0;">
        <a href="${resetLink}" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Reset Password</a>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">This link expires in 30 minutes.</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Request from:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Didn't request this?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 3. OTP Verification

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Your Verification Code</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Your verification code is:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0; text-align:center;">
        <p style="color:#333; font-size:20px; letter-spacing:5px; font-weight:bold; margin:0;">
            ${otpCode}
        </p>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">Expires in 10 minutes. Do not share with anyone.</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Request from:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Didn't request this?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 4. Account Verification

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Verify Your Account</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Please verify your account to get started:</p>
    <div style="text-align:center; margin:15px 0;">
        <a href="${verificationLink}" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Verify Account</a>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">Or copy this link:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0; word-break:break-all;">
        <p style="color:#555; margin:0; font-size:12px;">
            ${verificationLink}
        </p>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">Link expires in 24 hours.</p>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated message. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 5. Password Changed Confirmation

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Password Changed</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Your password was successfully changed:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:15px 0;">
        <a href="/account/security" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Review Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Wasn't you?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 6. Email Update Confirmation

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Email Address Updated</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Your email address has been updated:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>From:</strong> ${oldEmail}<br>
            <strong>To:</strong> ${newEmail}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:15px 0;">
        <a href="/account/security" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Review Activity</a>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Wasn't you?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 7. Two-Factor Authentication

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">2FA Status Changed</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Two-factor authentication has been ${status === 'enabled' ? 'enabled' : 'disabled'}:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Status:</strong> ${status === 'enabled' ? 'Enabled' : 'Disabled'}<br>
            <strong>Device:</strong> ${userAgent}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}
        </p>
    </div>
    <div style="text-align:center; margin:15px 0;">
        <a href="/account/security" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Review Security</a>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Wasn't you?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 8. Payment Receipt

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Payment Receipt</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Thank you for your payment:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>ID:</strong> ${transactionId}<br>
            <strong>Date:</strong> ${new Date().toGMTString()}<br>
            <strong>Amount:</strong> ${amount}<br>
            <strong>Method:</strong> ${paymentMethod}
        </p>
    </div>
    <table style="width:100%; border-collapse:collapse; margin:10px 0; font-size:13px;">
        <tr style="background:#f8f9fa;">
            <th style="padding:8px; text-align:left; border-bottom:1px solid #eee;">Item</th>
            <th style="padding:8px; text-align:right; border-bottom:1px solid #eee;">Amount</th>
        </tr>
        <tr>
            <td style="padding:8px; text-align:left; border-bottom:1px solid #eee;">${itemName}</td>
            <td style="padding:8px; text-align:right; border-bottom:1px solid #eee;">${itemPrice}</td>
        </tr>
        <tr>
            <td style="padding:8px; text-align:left;"><strong>Total</strong></td>
            <td style="padding:8px; text-align:right;"><strong>${amount}</strong></td>
        </tr>
    </table>
    <div style="text-align:center; margin:15px 0;">
        <a href="/account/billing" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Billing History</a>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated receipt. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 9. Account Deletion Confirmation

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Account Deletion Confirmed</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Your account deletion request is processed:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Account:</strong> ${userData.email}<br>
            <strong>Requested:</strong> ${new Date().toGMTString()}<br>
            <strong>Data removal:</strong> Within 30 days
        </p>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">Your data will be deleted per our Privacy Policy.</p>
    <div style="text-align:center; margin:15px 0;">
        <a href="/reactivate?token=${reactivationToken}" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Reactivate Account</a>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">You can reactivate within 30 days.</p>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Wasn't you?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 10. Event Reminder

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">Event Reminder</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">Reminder about your upcoming event:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Event:</strong> ${eventName}<br>
            <strong>Date:</strong> ${eventDate}<br>
            <strong>Time:</strong> ${eventTime}<br>
            <strong>Location:</strong> ${eventLocation}
        </p>
    </div>
    <div style="text-align:center; margin:15px 0;">
        <a href="/calendar/event/${eventId}" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">View Details</a>
    </div>
    <p style="color:#555; margin:5px 0; font-size:13px;">We look forward to seeing you!</p>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated reminder. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```

## 11. API Key Notification

```html
<div style="max-width:400px; margin:10px auto; font-family:Arial, sans-serif; padding:15px; border:1px solid #eee; border-radius:5px; box-shadow:0 1px 5px rgba(0,0,0,0.05);">
    <h3 style="color:#333; margin-top:0; margin-bottom:10px;">API Key ${action}</h3>
    <p style="color:#555; margin:5px 0;">Hi ${userData.fullName},</p>
    <p style="color:#555; margin:5px 0;">An API key has been ${action}:</p>
    <div style="background:#f8f9fa; padding:10px; border-radius:4px; margin:10px 0;">
        <p style="color:#555; margin:0; font-size:13px;">
            <strong>Key Name:</strong> ${keyName}<br>
            <strong>Action:</strong> ${action}<br>
            <strong>Time:</strong> ${new Date().toGMTString()}<br>
            <strong>IP:</strong> ${ipAddress}
        </p>
    </div>
    <div style="text-align:center; margin:15px 0;">
        <a href="/developer/api-keys" style="display:inline-block; padding:8px 16px; background:#0066cc; color:white; text-decoration:none; border-radius:3px; font-size:13px;">Manage Keys</a>
    </div>
    <div style="background:#fff8f8; border-left:3px solid #ff3b30; padding:8px; margin:10px 0;">
        <p style="color:#d32f2f; margin:0; font-size:12px;">
            <strong>Wasn't you?</strong> <a href="/support" style="color:#d32f2f;">Contact support</a>.
        </p>
    </div>
    <div style="color:#999; font-size:11px; text-align:center; border-top:1px solid #eee; padding-top:8px; margin-top:15px;">
        <p style="margin:5px 0;">Automated security notification. Do not reply.</p>
        <p style="margin:5px 0;">
            <a href="/account/preferences" style="color:#777; margin:0 5px;">Preferences</a>
            <a href="/privacy" style="color:#777; margin:0 5px;">Privacy</a>
            <a href="/help" style="color:#777; margin:0 5px;">Help</a>
        </p>
        <p style="margin:5px 0;">© 2025 Your Company. All rights reserved.</p>
    </div>
</div>
```
