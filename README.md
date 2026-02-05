# eIInvoice LT ReFirma

**eIInvoice LT ReFirma** is a specialized desktop utility developed for **La Tabacalera S.A.** to handle the bulk re-signing of Electronic Fiscal Interface (e-CF) documents for the Dominican Republic (DGII).

This tool is specifically designed to resolve issues with revoked or expired digital certificates by stripping old signatures and applying a fresh **RSA-SHA256** signature using a new `.p12` or `.pfx` certificate.

## Key Features
* **Massive Bulk Processing:** Add multiple XML files or folders and process them in a single batch.
* **Smart Renaming:** Automatically strips timestamp suffixes (e.g., `_05022026...`) to keep clean filenames like `eFact_1344_1627.xml`.
* **DGII Compliance:** * Implements **RSA-SHA256** signature method.
  * Uses **SHA256** digest method.
  * Preserves original XML whitespace to maintain signature integrity.
* **Automatic Timestamping:** Updates the `FechaHoraFirma` node to the current system time during the re-signing process.

## Technical Requirements
* **Framework:** .NET 6.0-windows or higher.
* **Dependencies:** `System.Security.Cryptography.Xml` (v8.0.0).
* **Certificate:** Valid `.p12` or `.pfx` file provided by an authorized CA (e.g., Viafirma).

## 💻 How to Use
1. **Certificate Configuration:** Browse for your `.p12` file and enter the password.
2. **Add Files:** Use "Add XML Files..." to select the invoices that need to be re-signed.
3. **Select Output:** Choose a destination folder where the cleaned, signed files will be saved.
4. **Re-sign:** Click **START RE-FIRMA**. View the real-time log for success/error reports.

## Security Note
This application does not store certificate passwords. Passwords must be entered manually for each session to ensure the security of the company's digital identity.

