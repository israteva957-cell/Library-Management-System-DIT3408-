# Library-Management-System-DIT3408-
A fully functional, real-time Library Management System (LMS) built for Central Metropolitan College as the DIT3408 IT Project Management Group Project (20%)

D – PROJECT EXECUTION



3.1	Project Design and Coding
System Flowchart (Mermaid – already provided earlier) Three Key Code Modules (taken and improved from the GitHub repo you linked: https://github.com/rajpra808/Library-Management-System)

Module 1: Firebase Initialization & Real-time Connection
JavaScript







This module initializes Firebase and establishes a persistent real-time connection to Cloud Firestore. It is imported in all pages (admin_portal.html, user_portal.html, index.html) so that every book added, borrowed, or returned instantly updates across all logged-in users without page refresh.

Module 2:  Add New Book (Admin Only)












This function runs exclusively in the admin portal. When the admin submits the “Add New Book” form, it creates a new document in the “books” collection with available copies automatically set. The onSnapshot listener instantly displays the new book in both admin and user dashboards.
Module 3: Borrow Book (User Portal)







When a student clicks “Borrow” on a book with available copies > 0, this function records the transaction and reduces the available count in real time. The admin immediately sees the updated availability without refresh.
 
3.2 Project Result
3.2.1	Library Portal Dashboard
 
Figure 2.0: Landing Page:  Library Portal (Main Entry Point of the System)

Figure 2: shows that elegant and highly professional landing page of the fully deployed Library Management System, titled “LIBRARY PORTAL: Your Digital Knowledge Gateway,” which serves as the single, intuitive entry point for all users at Central Metropolitan College. The modern dark-purple cosmic theme with glowing neon accents immediately conveys a contemporary digital experience. Two clearly separated, visually balanced portal cards dominate the screen: the left card labeled “Administrator” (purple glow) provides privileged access for library staff with the prominent “ADMIN ACCESS” button and lists advanced features such as System Configuration, Analytics & Reports, and User Management; the right card labeled “Member Portal” (cyan glow) targets students and faculty with the “MEMBER ACCESS” button and highlights user-centric functions including Browse Catalog, Borrow & Reserve, and Reading History. 
This clean separation enforces role-based access from the very first interaction, eliminates confusion, and sets the tone for a secure, user-friendly system. The design is fully responsive, working seamlessly on desktops, tablets, and smartphones, and directly reflects the successful execution of the UI/UX requirements defined in Part B while demonstrating that the system is live, visually polished, and ready for real-world deployment as of 30 November 2025. This landing page is the first screen every user sees upon visiting the public URL, instantly communicating professionalism and ease of use to both administrators and members.
3.2.2	Admin Portal
 
Figure 2.1: Admin Login Interface: Online Library Portal (Administrator Access)

The screenshot presents the dedicated and professionally designed Admin Authentication page of the Library Management System, accessible via 127.0.0.1:5500/admin_login.html during development and subsequently deployed to the live Firebase Hosting URL. This secure entry point enforces role-based access control by requiring valid administrator credentials before granting access to the full administrative dashboard. The interface adopts a sleek, modern dark cosmic theme with a prominent central card featuring a glowing shield icon symbolizing security, clearly titled “Online Library Portal – Administrator Access.” The authentication form is clean and user-friendly, consisting of two input fields (Username and Password) with appropriate icons, a visible “show password” toggle for convenience, and a prominent purple-gradient “LOGIN TO DASHBOARD” button that triggers Firebase Authentication verification. A “Forgot your password?” link is strategically placed for future password recovery implementation, while a functional “Back” button allows seamless return to the main landing page. 
This page exemplifies the successful execution of the security requirements defined in Part B’s Scope Statement and Software Project Plan, ensuring that only authorized library staff can manage the entire book inventory, user records, reports, and system configuration. The responsive layout, subtle glass-morphism effects, and consistent branding demonstrate high-quality UI/UX implementation, contributing directly to the project’s acceptance criteria of delivering a secure, intuitive, and visually polished administrative portal as part of the complete Library Management System delivered on 30 November 2025.

3.2.3	User Portal (Sign In )
 
Figure 2.2: User Portal (Sign In )
3.2.4	User Portal (Sign Up )

 
Figure 2.3: User/Member Login Interface: Online Library Portal (Member Access)
The screenshot showcases the dedicated User Authentication page designed specifically for students and faculty members of Central Metropolitan College, representing a critical component of the role-based access control architecture implemented in the Library Management System. Accessible via the live deployment or locally during development, this interface features the same elegant dark cosmic theme and glass-morphism design language as the admin portal, ensuring visual consistency and brand coherence across the entire application. The page clearly identifies itself as “Online Library Portal – Member Access” with a welcoming cyan-glow user icon, immediately distinguishing it from the administrative entry point. The authentication form offers a dual-mode toggle between Sign In and Sign Up, enabling both returning users to log in with existing credentials and new members to create accounts seamlessly  a direct fulfillment of the user onboarding requirement outlined in Part B’s Scope Statement. 
Input fields for Username and Password include intuitive icons and a password visibility toggle, while the prominent cyan “LOGIN” button triggers Firebase Authentication to securely verify credentials before granting access to the personalized member dashboard. The inclusion of a “Not registered? Create an account” prompt enhances usability and supports self-service registration, significantly improving user adoption rates. This professionally crafted, responsive, and secure login interface demonstrates successful execution of the planned authentication module, contributes directly to the project’s acceptance criteria of delivering an intuitive and inclusive digital library experience, and confirms that the system is fully operational and ready for campus-wide deployment as of 30 November 2025.
3.2.5	Add Book Portal
 
Figure 2.4: Add Book Portal

Administrator Dashboard of the Library Management System, accessed immediately after successful authentication through the secure admin login portal. This interface serves as the central command center for all library operations at Central Metropolitan College and demonstrates the successful execution of the role-based access control and real-time data integration planned in Part B. The clean, modern purple-themed layout clearly identifies the logged-in user as “Admin User  Library Manager” with a prominent “Logout” button for session security. Two powerful search modules dominate the top section: “Search Students” (by name or ID) and “Search Books” (by title or author), each equipped with real-time filtering and “Show All” buttons that instantly populate the large results area below using Firebase Firestore’s onSnapshot listeners. At the bottom, two vibrant action buttons  “+ Add New Books” (cyan) and “Buy Books” (orange gradient) provide one-click access to inventory management functions. 
The spacious results panel displays a placeholder message with a checkmark icon when idle, transforming dynamically into detailed tables upon query execution. This dashboard exemplifies the project’s core deliverables: real-time synchronization, intuitive administrative controls, responsive design across devices, and a professional user experience that significantly reduces manual workload. Its successful implementation confirms that the system not only meets but exceeds the functional and non-functional requirements defined in the Scope Statement and Software Project Plan
3.2.6	Search Student
 
Figure 2.5: Add Book Portal 
3.2.7	Search Books
 
Figure 2.6: Search Book
3.2.8	Add New Book
 
Figure 2.7: Add New Book

Management System: real-time retrieval and presentation of student borrowing records from Firebase Cloud Firestore. After the admin performs a “Show All Students” action, the previously empty results panel instantly populates with a clean, card-based layout containing five student profiles (Alice Johnson, Bob Smith, Carol Williams, David Brown, and Emma Davis), each clearly displaying the student’s full name, unique ID, registered email address, and current number of books borrowed. 
This dynamic rendering is powered entirely by Firestore’s onSnapshot real-time listener, ensuring that any change in borrowing status whether a book is issued or returned from the member portal  is reflected immediately across all admin sessions without requiring manual refresh. The persistent presence of the dual search bars (Students and Books), action buttons (“+ Add New Books” and “Buy Books”), and secure logout option reinforces the dashboard’s role as a comprehensive management hub. This screen provides concrete visual evidence that the planned integration between frontend JavaScript and the cloud backend has been flawlessly executed, delivering instantaneous data consistency, accurate user management, and complete administrative oversight as specified in the original scope and acceptance criteria.

3.2.9	Buy Book
 
Figure 2.8: Buy Book
A value-added administrative feature successfully implemented during the execution phase to streamline procurement and supplier relationship management at Central Metropolitan College. Accessed via the main administrator dashboard, this module displays verified book supplier contacts in an elegant, card-based layout with a professional purple gradient design consistent with the overall system branding. Two verified retailers “Eva Israt” and “Ms. Nur Anissya” are shown with their full names, official email addresses, contact numbers, and associated Google business profiles, each marked with a green “Verified” badge to indicate pre-approved status within the system. Action buttons for direct “Email” and “Call” communication are prominently placed on every card, enabling the library manager to instantly reach suppliers for new purchases or restocking without leaving the portal. 
A “+ Add New Retailer” button at the bottom supports future expansion of the supplier database. This module demonstrates successful extension beyond the original scope while remaining fully aligned with the project’s objective of creating a comprehensive digital ecosystem for library operations. Its seamless integration with the existing real-time Firebase backend and responsive design further validates the robustness of the architecture planned in Part B and executed during the final sprint.
 

