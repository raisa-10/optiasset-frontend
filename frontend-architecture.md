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
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <UserDataTable /> - Searchable and filterable table of all users  
Component: <AddUserModal /> - Form to create a new user  
Component: <EditUserModal /> - Update existing user details  
Component: <DeleteUserConfirmation /> - Confirmation dialog before deletion  

---

### Page: /assets
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <AssetDataTable /> - Displays all company assets with pagination  
Component: <AddAssetModal /> - Add new asset form  
Component: <EditAssetModal /> - Update asset details  
Component: <AssetStatusBadge /> - Displays status (Available, Assigned, Broken)  

---

### Page: /assignments
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <AssignmentTable /> - Shows asset assignment history  
Component: <AssignAssetModal /> - Assign asset to a user  
Component: <ReturnAssetButton /> - Mark asset as returned  

---

### Page: /reports
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <AssetUtilizationChart /> - Visual graph of asset usage  
Component: <BrokenAssetsList /> - List of damaged assets  
Component: <ExportReportButton /> - Download report as CSV or PDF  

---

## Role: Asset Manager
(Can manage assets and assignments but not users)

### Page: /dashboard
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <StatCards />  
Component: <RecentAssignmentsTable />  

---

### Page: /assets
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <AssetDataTable />  
Component: <AddAssetModal />  
Component: <EditAssetModal />  

---

### Page: /assignments
Component: <Sidebar />  
Component: <TopNavbar />  
Component: <AssignmentTable />  
Component: <AssignAssetModal />  
Component: <ReturnAssetButton />  

---

## Role: Standard Employee
(Can only view assets assigned to them)

### Page: /my-assets
Component: <TopNavbar />  
Component: <MyAssetList /> - Grid view of assigned devices  
Component: <AssetDetailsModal /> - View detailed information  
Component: <ReportIssueButton /> - Report if asset is broken  

---

### Page: /profile
Component: <TopNavbar />  
Component: <ProfileDetailsCard /> - Displays personal details  
Component: <ChangePasswordForm /> - Allows password update  

---

## Common Pages (Accessible to All Roles)

### Page: /login
Component: <LoginForm /> - Email and password fields  
Component: <BrandLogo />  

---

### Page: /forgot-password
Component: <ForgotPasswordForm />  

---

### Page: /reset-password
Component: <ResetPasswordForm />  

---