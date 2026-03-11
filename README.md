# Cray Payments for WooCommerce

Welcome to the official **Cray Payments** plugin for WooCommerce. This plugin allows you to accept payments on your WordPress store using Cray's secure payment infrastructure.

## 🚀 Features
*   **Card Payments**: Accept Visa, Mastercard, and Verve cards securely.
*   **Mobile Money (MoMo)**: Support for mobile money payments across multiple African countries (Nigeria, Ghana, Kenya, etc.).
*   **3D Secure**: Full support for 3D Secure (3DS) authentication to prevent fraud.
*   **Webhooks**: Automatic order status updates via webhooks.
*   **Subaccounts**: Support for splitting payments to subaccounts.
*   **Secure**: Sensitive card data is never stored on your server.

---

## 🛠️ Installation & Setup

### **Step 1: Install the Plugin**
1.  Download the plugin zip file.
2.  Log in to your WordPress Admin Dashboard.
3.  Go to **Plugins** > **Add New**.
4.  Click **Upload Plugin** at the top.
5.  Choose the zip file you downloaded and click **Install Now**.
6.  After installation, click **Activate**.

### **Step 2: Enable the Payment Gateway**
1.  Go to **WooCommerce** > **Settings**.
2.  Click on the **Payments** tab.
3.  Find **Cray Payments** and toggle the switch to **Enable**.
4.  Click **Manage** (or "Set up") next to Cray Payments to configure your settings.

### **Step 3: Configure API Keys**
You need your API keys from your Cray Dashboard.
1.  **Environment**: Select `Sandbox` for testing or `Live` for real payments.
2.  **Public Key**: Enter your Cray Public Key.
3.  **Secret Key**: Enter your Cray Secret Key.
4.  **Default Currency**: Select the currency you want to process payments in (e.g., USD, NGN).
5.  Click **Save Changes**.

### **Step 4: Configure Webhooks (Important!)**
Webhooks allow Cray to notify your store when a payment is successful, ensuring orders are updated even if the user closes their browser.
1.  In the plugin settings page, look for the **Webhook Endpoint** field.
2.  Copy the URL (e.g., `https://yourstore.com/wp-json/cray/v1/webhook`).
3.  Log in to your **Cray Dashboard**.
4.  Navigate to **Settings** > **Webhooks**.
5.  Paste the URL and save.

---

## 💳 Payment Methods

You can choose which payment methods to display on checkout by going to the main Cray settings page (usually under a "Cray Payments" submenu or the main plugin settings).

*   **Card Only**: Show only the credit/debit card form.
*   **MoMo Only**: Show only the Mobile Money option.
*   **Both**: Allow customers to choose between Card and MoMo.

---

## 🧪 Testing (Sandbox Mode)

1.  Ensure **Environment** is set to `Sandbox` in the plugin settings.
2.  Use the test cards provided in the Cray documentation to simulate successful and failed transactions.
3.  Check the **WooCommerce > Status > Logs** (select `cray-woocommerce-gateway` from the dropdown) to debug any issues.

---

## ❓ Frequently Asked Questions

**Q: Where can I find my API Keys?**
A: Log in to your Cray Dashboard and navigate to the Developer/API Settings section.

**Q: My orders are not updating to "Processing" after payment.**
A: Ensure you have configured the **Webhook URL** correctly in your Cray Dashboard (see Step 4).

**Q: Is this plugin secure?**
A: Yes. Card details are tokenized and processed securely by Cray. We do not store sensitive card information (PAN, CVV) on your server.

---

## 📞 Support
If you encounter any issues, please check the logs in **WooCommerce > Status > Logs** or contact Cray support.