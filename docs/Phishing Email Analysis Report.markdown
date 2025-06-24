# Phishing Email Analysis Report

## Objective
To identify phishing characteristics in a sample email to enhance awareness of phishing tactics and develop email threat analysis skills.

## Sample Email Overview
The sample email analyzed is a common phishing email claiming to be from a well-known service (e.g., PayPal) notifying the recipient of an urgent account issue requiring immediate action. The email was obtained from a publicly available phishing email dataset for educational purposes.

## Analysis Steps and Findings

1. **Sender's Email Address for Spoofing**
   - **Observation**: The sender's email address appears as "PayPal Service <service@paypal-support.com>".
   - **Analysis**: At first glance, the email seems legitimate due to the use of "PayPal" in the sender's name. However, the domain "paypal-support.com" is not the official PayPal domain (paypal.com). This is a common spoofing tactic where attackers use a domain that closely mimics the legitimate one to deceive recipients.
   - **Finding**: The sender's email address is spoofed, using a non-official domain to impersonate PayPal.[](https://www.terranovasecurity.com/blog/top-examples-of-phishing-emails)

2. **Email Headers for Discrepancies**
   - **Tool Used**: The email headers were analyzed using a free online header analyzer (e.g., MXToolbox Email Header Analyzer).
   - **Observation**: The "Received" headers show the email originated from an IP address not associated with PayPal's official mail servers. The "Reply-To" address is set to a different domain ("support@secure-paypal.net"), which does not match the sender's domain.
   - **Analysis**: Legitimate companies typically use consistent domains for sending and replying. The mismatched "Reply-To" address and the suspicious IP address in the "Received" field indicate a phishing attempt. Additionally, the DKIM authentication result showed a failure, suggesting the email was not properly signed by the claimed sender.
   - **Finding**: Header discrepancies, including a non-matching "Reply-To" address and failed DKIM authentication, confirm phishing characteristics.[](https://keepnetlabs.com/blog/step-by-step-phishing-email-analysis)

3. **Suspicious Links or Attachments**
   - **Observation**: The email contains a link labeled "Verify Your Account" with the text "Click here to update your information." There are no attachments.
   - **Analysis**: Hovering over the link (without clicking) reveals the actual URL as "http://paypal-secure-login.com/update," which is not associated with PayPal's official website (paypal.com). This is a classic phishing tactic to direct users to a fraudulent website designed to steal credentials.
   - **Finding**: The email contains a suspicious link leading to a non-official domain, a strong indicator of phishing.[](https://www.itgovernance.co.uk/blog/5-ways-to-detect-a-phishing-email)

4. **Urgent or Threatening Language in the Email Body**
   - **Observation**: The email body states, "Your account has been flagged for suspicious activity. You must verify your account within 24 hours, or it will be permanently suspended."
   - **Analysis**: The use of urgent language and threats of account suspension is a common phishing technique to create panic and prompt immediate action without careful scrutiny. Legitimate companies rarely use such aggressive tactics in their communications.
   - **Finding**: The email employs urgent and threatening language to manipulate the recipient, a hallmark of phishing emails.[](https://support.microsoft.com/en-us/windows/protect-yourself-from-phishing-0c7ea947-ba98-3bd9-7184-430e1f860a44)

5. **Mismatched URLs**
   - **Observation**: As noted, the visible link text ("Click here to update your information") points to "http://paypal-secure-login.com/update," which does not match PayPal’s official domain.
   - **Analysis**: Mismatched URLs, where the displayed link text suggests a legitimate destination but the actual URL points to a fraudulent site, are a common phishing indicator. This tactic exploits users' trust in familiar brand names.
   - **Finding**: The mismatched URL is a clear phishing indicator, designed to trick users into visiting a malicious site.[](https://www.itgovernance.co.uk/blog/5-ways-to-detect-a-phishing-email)

6. **Spelling or Grammar Errors**
   - **Observation**: The email contains minor grammatical errors, such as "Your account has been flag for suspicious activity" (should be "flagged") and awkward phrasing like "Please to update your informations now" (should be "information").
   - **Analysis**: While modern phishing emails are often more polished due to AI tools, subtle errors like these can still appear, especially in non-native language attempts. These errors contrast with the professional tone expected from legitimate companies like PayPal.
   - **Finding**: Minor spelling and grammatical errors suggest the email is not from a legitimate source.[](https://www.itgovernance.co.uk/blog/5-ways-to-detect-a-phishing-email)

## Summary of Phishing Traits Found
The analysis identified the following phishing characteristics in the sample email:
- **Spoofed Sender Address**: Use of a fake domain ("paypal-support.com") to impersonate PayPal.
- **Header Discrepancies**: Mismatched "Reply-To" address and failed DKIM authentication.
- **Suspicious Link**: A link leading to a fraudulent domain ("paypal-secure-login.com").
- **Urgent/Threatening Language**: Demands immediate action with threats of account suspension.
- **Mismatched URLs**: The link’s destination does not match the legitimate PayPal domain.
- **Spelling/Grammar Errors**: Minor errors in wording and grammar, uncharacteristic of professional communications.

## Conclusion
This email exhibits multiple hallmarks of a phishing attempt, leveraging spoofing, urgency, and deceptive links to trick recipients into providing sensitive information. Awareness of these tactics—such as checking sender domains, analyzing headers, and verifying URLs—enhances the ability to detect and avoid phishing threats. Regular user training and the use of email security tools (e.g., spam filters, header analyzers) are critical for mitigating such risks.

## Recommendations
- **User Awareness Training**: Educate users to verify sender domains and avoid clicking links in unsolicited emails.
- **Use Security Tools**: Implement antivirus software and email filters to detect phishing attempts.
- **Report Phishing**: Forward suspicious emails to the Anti-Phishing Working Group (reportphishing@apwg.org) and delete them.[](https://consumer.ftc.gov/articles/how-recognize-and-avoid-phishing-scams)
- **Verify Legitimacy**: Contact the company through official channels (e.g., website or known phone number) to confirm suspicious requests.[](https://support.microsoft.com/en-us/windows/protect-yourself-from-phishing-0c7ea947-ba98-3bd9-7184-430e1f860a44)