# 🎓 ServiceNow Administration Fundamentals (Xanadu)

**Platform:** Now Learning  
**Link:** [ServiceNow Administration Fundamentals – Xanadu](https://learning.servicenow.com/lxp/en/now-platform/servicenow-administration-fundamentals-on-demand?id=learning_course_prev&course_id=400ce92b47530e10123f3975d36d43f1)  
**Status:** 🚧 In Progress

---

## 📚 What I'm Learning

- **Table and Data Management:** Creating custom tables and configuring fields.
- **Forms and Lists Customization:** Enhancing data interaction through UI configurations.
- **User and Data Management:** Managing users, roles, and access controls.
- **Platform Features:** Exploring workflows, knowledge management, and automation basics.

---

## 💬 Notes

This course has been a great deep dive into the core administrative functions of ServiceNow as I prepare for my **CSA certification**. 

### 📝 Handling a Real-World Challenge in Lab 4.1.1

While working on **Lab 4.1.1: Create Table for HHD Configuration Records**, I encountered an interesting challenge — adding the `Assigned to.Email` field to the Holographic Handheld Devices (HHDs) list view.

I discovered that ServiceNow doesn’t always allow direct dot-walking for reference fields in list layouts. To solve this, I created a **Function Field** that dynamically pulls the email from the `Assigned to` user:

```plaintext
1. Created a String field called 'Assigned to Email'.
2. Enabled 'Function Field' and set the function to: assigned_to.email
3. Set Max Length to 100.
4. Added the new field to the list layout.
