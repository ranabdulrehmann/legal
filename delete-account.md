# Request Account Deletion

**QuickScan PDF**

You can request deletion of your QuickScan PDF account and its associated data from this page, without needing to install or open the App.

## What gets deleted

- Your linked Google account (email, name) and profile fields (phone, birth year, country) are removed.
- Your coin balance, streak, and reward history tied to that account are removed.
- Documents you scanned are **not affected by this request** — they are stored only on your own device and were never sent to us. Deleting the App or the documents themselves is done on your device, separately from this request.

## How it works

1. We soft-delete your account immediately upon a verified request: it is deactivated and excluded from normal use (you will not be able to sign in with it again).
2. Your account data is permanently and irreversibly deleted no later than **30 days** after the request, as part of our regular deletion sweep. We keep it briefly rather than deleting it instantly so we can resolve a request made in error (for example, if someone else submits this form using your email by mistake) and to meet basic fraud-prevention and accounting obligations.
3. If you have an active Pro subscription purchased through Google Play, please cancel it in [Google Play's subscriptions page](https://play.google.com/store/account/subscriptions) first — deleting your account does not cancel a running subscription, and Google will continue to bill you for it independently of this request.

## Submit a request

Fill in the form below, or simply email us directly at **apexbyte.technologies@openbase.network** with the subject "Delete my QuickScan PDF account" and the email address linked to your account.

<form id="delete-account-form" style="max-width: 420px; display: flex; flex-direction: column; gap: 0.75rem; margin-top: 1rem;">
  <label for="name">Your name</label>
  <input type="text" id="name" placeholder="Jane Doe" required style="padding: 0.5rem;" />
  <label for="email">Email address linked to your QuickScan PDF account</label>
  <input type="email" id="email" placeholder="you@example.com" required style="padding: 0.5rem;" />
  <button type="submit" style="padding: 0.6rem 1rem; cursor: pointer;">Open email to submit request</button>
</form>

<p style="font-size: 0.85em; color: #666;">This button opens your device or computer's own email app with a pre-filled message to us — this page does not submit anything itself or store what you type.</p>

<script>
  document.getElementById('delete-account-form').addEventListener('submit', function (event) {
    event.preventDefault();
    var name = document.getElementById('name').value;
    var email = document.getElementById('email').value;
    var subject = encodeURIComponent('Delete my QuickScan PDF account');
    var body = encodeURIComponent('Name: ' + name + '\nAccount email: ' + email + '\n\nPlease delete my QuickScan PDF account and associated data.');
    window.location.href = 'mailto:apexbyte.technologies@openbase.network?subject=' + subject + '&body=' + body;
  });
</script>

We will confirm receipt and complete the deletion within 30 days, usually much sooner. See our [Privacy Policy](privacy) for your other rights, and [Terms of Use](terms) for the full terms governing the App.
