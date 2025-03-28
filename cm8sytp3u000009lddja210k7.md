---
title: "How to Apply for an M-Pesa Paybill Number or Till Number and setup API"
seoTitle: "M-Pesa Paybill and Till Number Application Guide"
seoDescription: "Learn how to apply for an M-Pesa Paybill or Till Number for seamless business transactions with this step-by-step guide"
datePublished: Fri Mar 28 2025 15:56:54 GMT+0000 (Coordinated Universal Time)
cuid: cm8sytp3u000009lddja210k7
slug: m-pesa-paybill-number-or-till-number-application-and-api-setup
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1743177236209/a9f5ef22-736d-49c4-9f74-c7799ed1c30e.png
tags: mpesa, daraja-api, paybill

---

To integrate M-Pesa payments into your business, you need to apply for either a Paybill Number or a Till Number. Below is a step-by-step guide on how to apply for each.

---

# **M-Pesa Paybill & Till Application Guide**

## **1\. Paybill vs. Till – Which One Should You Choose?**

Before starting the application process, it's important to determine whether you need a **Paybill** or a **Till (Buy Goods & Services)**.

### **Which One is Best for You?**

| Feature | **Paybill** | **Till (Buy Goods & Services)** |
| --- | --- | --- |
| **Use Case** | Best for businesses needing to track customer payments (e.g., utilities, schools, online businesses). | Best for merchants collecting payments at physical stores (e.g., shops, restaurants, supermarkets). |
| **Transaction Identifier** | Requires an **account number**, making it easy to track customer payments. | No account number required—transactions are processed instantly. |
| **Ideal for Online Payments?** | ✅ Yes, supports **STK Push** and detailed transaction tracking. | ✅ Yes, but primarily suited for direct payments. |
| **Settlement Options** | Funds settle to a **business bank account**. | Funds settle to an **M-Pesa wallet** or **business bank account** (optional). |
| **Scalability** | ✅ Ideal for businesses with **multiple branches & online integrations**. | 🚫 Limited scalability—best for small businesses. |

💡 **Best Choice for Online Integration:** Always opt for a **Paybill Number**, as it provides both STK Push and enhanced tracking capabilities.

---

## **2\. Requirements for Paybill & Till Application**

To apply for a Paybill or Till, you must gather the following documents:

✅ **Application Form** – [**\[Download Form\]**](https://www.safaricom.co.ke/images/Downloads/M-PESA_Account_Opening_Authorization_Form_2020.pdf)  
✅ **Tariff Guide** – [**\[Download Form\]**](https://www.safaricom.co.ke/images/Downloads/M-Pesa-Paybill-Tariff-guide.pdf)  
✅ **KRA PIN Certificate**  
✅ **Copies of ID/Passport** (for business owners or administrators)  
✅ **Account Opening Form** – [**\[Download Form\]**](https://www.safaricom.co.ke/images/Downloads/Mpesa-account-opening-authorization-form.pdf)  
✅ **Administrator Details Form** – [**\[Download Form\]**](https://www.safaricom.co.ke/images/Downloads/M-PESA-Business-Administator-Form.pdf)  
✅ **Bank Letter / Canceled Cheque** (for bank settlements)  
✅ **Administrator’s Letter** – Write a letter with company/business letter head in pdf

### **Important Notes:**

* All letters and forms **must be stamped**.
    
* The **bank letter must be signed or stamped** by the issuing bank.
    
* 🚨 **Personal Tills & Bank Paybills Cannot Be Used for Online Integration**. If you have a **personal Till or Bank Paybill**, use a third-party service like **Lipia-Online** to enable online M-Pesa payments.
    

---

## **3\. How to Apply for a Paybill or Till Number**

Once you have all the required documents:

### **Step 1: Scan Your Documents**

### **Step 2: Send an Email to Safaricom**

📩 **To:** [**M-PESABusiness@safaricom.co.ke**](mailto:M-PESABusiness@safaricom.co.ke)  
📩 **CC:** [**paybill@safaricom.co.ke**](mailto:paybill@safaricom.co.ke)  
📌 **Subject:** Paybill/Till Application Request

💡 **Email Body Template:**

> ***Dear Safaricom Business Team,***
> 
> ***I would like to apply for a \[Paybill/Till\] number for my business. Below are the details:***
> 
> * ***Business Name: \[Your Business Name\]***
>     
> * ***Business Type: \[Company/Sole Proprietorship/Partnership\]***
>     
> * ***Contact Person: \[Your Name\]***
>     
> * ***Phone Number: \[Your Phone\]***
>     
> * ***Email Address: \[Your Email\]***
>     
> * ***Settlement Option: \[M-Pesa Wallet / Business Bank Account\]***
>     
> 
> ***I have attached all the necessary documents for your review. Kindly process my request and let me know if any additional information is needed.***
> 
> ***Thank you.***

📌 **Attachments:** Attach the **scanned PDF of all documents**.

### **Step 3: Processing & Approval**

* Safaricom typically processes applications **within 72 hours**.
    
* If you **don’t receive feedback within 24 hours**, double-check your documents and **resend your application**.
    

---

## **4\. What to Expect After Application**

If your Paybill or Till is approved, you will receive an **SMS notification** with your payment details.

### **For Paybill:**

> ***"Dear \[Name\], Paybill account has been activated for \[Business Name\]. Paybill Number: \[ShortCode\]. Thank you."***

### **For Till:**

> ***"Your Buy Goods Till has been activated. Till Number: \[XXXXX\], Store Number: \[XXXXX\]."***

---

## **5\. Requesting Admin Credentials for Online Integration**

🔹 **Receiving the SMS is Not Enough!**  
For online M-Pesa integration via the **Daraja API**, you must also receive **admin credentials** to access Safaricom’s developer portal.

🔹 **If You Didn’t Receive Admin Credentials:**  
If Safaricom assumes your Paybill/Till is for **physical store use**, they may **not create an admin account** by default.

📌 **Solution:** Send a follow-up email **requesting admin account creation.**

📩 **To:** [**M-PESABusiness@safaricom.co.ke**](mailto:M-PESABusiness@safaricom.co.ke)  
📩 **CC:** [**apisupport@safaricom.co.ke**](mailto:apisupport@safaricom.co.ke)  
📌 **Subject:** Request for Admin Account Creation

💡 **Email Body Template:**

> ***Dear Safaricom Business Team,***
> 
> ***I recently applied for a \[Paybill/Till\] and received confirmation via SMS. However, I did not receive admin credentials to access the M-Pesa Portal***
> 
> ***Please create my admin account for online integration. I have reattached all the required documents, with the Administrator’s Letter as the first page.***
> 
> ***Business Details:***
> 
> * ***Paybill/Till Number: \[Your Number\]***
>     
> * ***Business Name: \[Your Business Name\]***
>     
> * ***Admin Contact: \[Your Name & Phone\]***
>     
> 
> ***Kindly process this request as soon as possible. Thank you.***

📌 **Attachments:** Attach all **original documents**, with the **Administrator’s Letter as the first page**.

### **Expected Response from Safaricom:**

If approved, you’ll receive an **email with admin login details** for the mpesa portal([**https://org.ke.m-pesa.com**](https://org.ke.m-pesa.com/))

📧 **Example:**

> ***"Your M-Pesa user account for \[Paybill/Till Number\] - \[Business Name\] has been created.  
> Username: \[Your Username\]  
> Password: \[Your Password\]"***

---

## **6\. Logging into the M-Pesa Organization Portal & Setting Up Daraja API**

Once you receive your **admin credentials**, you need to log in to the **M-Pesa Organization Portal** to manage your Paybill/Till and create **API operators** for integration with Daraja.

### **Step 1: Access the M-Pesa Organization Portal**

🔗 **Go to:** [**https://org.ke.m-pesa.com/**](https://org.ke.m-pesa.com/)

### **Step 2: Log In with Your Admin Credentials**

📌 **Enter your:**

* **Username** (provided in the email from Safaricom)
    
* **Password** (provided in the same email)
    

🔹 **First-time login?** You will be required to **change your password** for security purposes.

---

### **Step 3: Create Operators for Daraja API Access**

After logging in, you need to create two operators **Business Manager** and **API Operator.**

**Why Do You Need Both?**  
The **Business Manager** role is necessary because it allows you to set passwords for API Operators. Without it, you won’t be able to generate secure API credentials.

#### **📌 How to Create an Business Manager:**

1. **Go to** the "Operator Management" section.
    
    → My Function → Operator Managent
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743174532849/ddb2b80c-dada-4a7d-b007-32cfde1bea75.png?auto=compress,format&format=webp&q=75 align="left")
    
2. Click **Create Operator**.
    
3. Fill in the required details:
    
    * **Access Channel:** Select "web."
        
    * **Username:** Choose a name (e.g., `business_manager`).
        
    * **Rule Profile:** Select “web profile default rule profile”
        
    * **For roles:** Select “Business Manager” and “Set Restricted ORG API PASSWORD”
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743175016067/28dd1c9f-e71e-4ca5-a875-344664b1ba69.png?auto=compress,format&format=webp&q=75 align="left")
        
    * **Enter the KYC info**
        
4. Click **Submit** and wait for a confirmation email or sms.
    

---

### **Step 4: Setup API Operator**

1. Navigate to operator management
    
2. Click **Create Operator**.
    
3. Fill in the required details:
    
    * **Access Channel:** Select "api."
        
    * **Username:** Choose a name (e.g., api\_operator).
        
    * **Rule Profile:** Select “web profile default rule profile”
        
    * **For roles:** For API Operator, select ONLY the roles necessary for API usage. Selecting all roles may lead to security risks.
        
        ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743175472052/b50d5a27-594e-4c50-9589-f84fba7cc3ae.png?auto=compress,format&format=webp&q=75 align="left")
        
    * **Enter the KYC info**
        
4. Click **Submit** and wait for a confirmation email or sms.
    
5. Logout from the admin account and login using the business manager credentials.
    
6. Go to Operator management. At first it may not show up the operators but click search to refresh.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743175957969/b1f608a1-a7a6-4334-9cca-b392c377fb03.png?auto=compress,format&format=webp&q=75 align="left")
    
7. On the `api_operator` row press edit button on operation column. It would redirect to operator info
    
8. Click `set password` and set new strong password
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743176106079/e71f521d-479e-414b-b0d3-640831cfe24f.png?auto=compress,format&format=webp&q=75 align="left")
    
    ✅ Now your credentials are good to go!!!
    

---

### **Step 5: Going Live**

Now that your API operator is set up, you can retrieve the **Consumer Key & Consumer Secret** required for Daraja API integration.

📌 **How to get your API credentials:**

1. Log in to [**https://developer.safaricom.co.ke/**](https://developer.safaricom.co.ke/).
    
2. Navigate to go live
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743176347043/64bd9eb3-5d1a-437a-9467-c4067c36a5cf.png?auto=compress,format&format=webp&q=75 align="left")
    
3. Follow the procedure to connect your short code to daraja.
    
4. Navigate to **My Apps**. A new production app would have been automatically created
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1743176643646/2e9f4331-8332-4b4e-aa25-8aad84cb14f8.png?auto=compress,format&format=webp&q=75 align="left")
    
5. Copy your **Consumer Key & Consumer Secret**
    
6. Store them securely for API integration.
    

✅ Now your Paybill/Till is fully integrated with the **M-Pesa Daraja API** and ready to process online transactions! 🚀

✅ For any clarification or support [apisupport@safaricom.co.ke](mailto:apisupport@safaricom.co.ke)