# OptiAsset - Frontend Architecture Document
Framework: Next.js  
Architecture Pattern: Role-Based UI Structure  
Project Type: IT Asset Management System  

---

## Role: IT Administrator
(Full access to manage users, assets, assignments, and reports)

### Page: /dashboard
Component: <Sidebar /> - Navigation links (Dashboard, Users, Assets, Assignments, Reports)  
Component: <TopNavbar /> - Logged-in profile display and logout button  
Component: <StatCards /> - Displays Total Assets, Assigned Assets, Available Assets, Broken Assets  
Component: <RecentAssignmentsTable /> - Shows the latest 5 asset assignments  
Component: <QuickActionButtons /> - Shortcuts for Add User and Add Asset  

---

### Page: /users
Component: <Sidebar /> - Reusable navigation panel  
Component: <TopNavbar /> - User profile and logout  
Component: <UserDataTable /> - Searchable and filterable table of all users  
Component: <AddUserModal /> - Form to create a new user  
Component: <EditUserModal /> - Update existing user details  
Component: <DeleteUserConfirmation /> - Confirmation dialog before deletion  

---

### Page: /assets
Component: <Sidebar /> - Reused navigation  
Component: <TopNavbar /> - Header section  
Component: <AssetDataTable /> - Displays all company assets with pagination  
Component: <AddAssetModal /> - Add new asset form  
Component: <EditAssetModal /> - Update asset details  
Component: <AssetStatusBadge /> - Displays status (Available, Assigned, Broken)  

---

### Page: /assignments
Component: <Sidebar /> - Navigation panel  
Component: <TopNavbar /> - Header  
Component: <AssignmentTable /> - Shows asset assignment history  
Component: <AssignAssetModal /> - Assign asset to a user  
Component: <ReturnAssetButton /> - Mark asset as returned  

---

### Page: /reports
Component: <Sidebar /> - Navigation  
Component: <TopNavbar /> - Header  
Component: <AssetUtilizationChart /> - Visual graph of asset usage  
Component: <BrokenAssetsList /> - List of damaged assets  
Component: <ExportReportButton /> - Download report as CSV or PDF  

---

## Role: Asset Manager
(Can manage assets and assignments but not users)

### Page: /dashboard
Component: <Sidebar /> - Navigation links  
Component: <TopNavbar /> - User profile section  
Component: <StatCards /> - Overview of asset status  
Component: <RecentAssignmentsTable /> - Recent assignment list  

---

### Page: /assets
Component: <Sidebar /> - Navigation  
Component: <TopNavbar /> - Header  
Component: <AssetDataTable /> - List of all assets  
Component: <AddAssetModal /> - Add new asset  
Component: <EditAssetModal /> - Update asset  

---

### Page: /assignments
Component: <Sidebar /> - Navigation  
Component: <TopNavbar /> - Header  
Component: <AssignmentTable /> - List of assignments  
Component: <AssignAssetModal /> - Assign asset to user  
Component: <ReturnAssetButton /> - Return assigned asset  

---

## Role: Standard Employee
(Can only view assets assigned to them)

### Page: /my-assets
Component: <TopNavbar /> - Profile and logout  
Component: <MyAssetList /> - Grid view of assigned devices  
Component: <AssetDetailsModal /> - View detailed information  
Component: <ReportIssueButton /> - Report if asset is broken  

---

### Page: /profile
Component: <TopNavbar /> - Header  
Component: <ProfileDetailsCard /> - Displays personal details  
Component: <ChangePasswordForm /> - Allows password update  

---

## Common Pages (Accessible to All Roles)

### Page: /login
Component: <LoginForm /> - Email and password input fields  
Component: <BrandLogo /> - Application logo  

---

### Page: /forgot-password
Component: <ForgotPasswordForm /> - Enter email to reset password  

---

### Page: /reset-password
Component: <ResetPasswordForm /> - Enter new password  

---