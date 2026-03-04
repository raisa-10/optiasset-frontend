# OptiAsset - Frontend Architecture Document
Framework: Next.js
Architecture Type: Role-Based UI Mapping

--------------------------------------------

Role: IT Administrator (Full access to manage users, assets, and assignments)

Page: /dashboard
Component: <Sidebar /> - Navigation (Dashboard, Assets, Users, Assignments, Reports)
Component: <TopNavbar /> - Profile dropdown and logout
Component: <StatCards /> - Total Assets, Assigned Assets, Available Assets, Broken Assets
Component: <RecentAssignmentsTable /> - Last 5 assignments overview
Component: <QuickActionsPanel /> - Add Asset / Add User shortcuts

Page: /users
Component: <Sidebar />
Component: <TopNavbar />
Component: <UserDataTable /> - Table with search and filter
Component: <AddUserModal /> - Form popup
Component: <EditUserModal />
Component: <DeleteUserConfirmation />

Page: /assets
Component: <Sidebar />
Component: <TopNavbar />
Component: <AssetDataTable /> - Search, filter, pagination
Component: <AddAssetModal />
Component: <EditAssetModal />
Component: <AssetStatusBadge />

Page: /assignments
Component: <Sidebar />
Component: <TopNavbar />
Component: <AssignmentTable />
Component: <AssignAssetModal />
Component: <ReturnAssetButton />

Page: /reports
Component: <Sidebar />
Component: <TopNavbar />
Component: <AssetUtilizationChart />
Component: <BrokenAssetsList />
Component: <ExportReportButton />

--------------------------------------------

Role: Asset Manager (Manages assets and assignments only)

Page: /dashboard
Component: <Sidebar />
Component: <TopNavbar />
Component: <StatCards />
Component: <RecentAssignmentsTable />

Page: /assets
Component: <Sidebar />
Component: <TopNavbar />
Component: <AssetDataTable />
Component: <AddAssetModal />
Component: <EditAssetModal />

Page: /assignments
Component: <Sidebar />
Component: <TopNavbar />
Component: <AssignmentTable />
Component: <AssignAssetModal />
Component: <ReturnAssetButton />

--------------------------------------------

Role: Standard Employee (View only access to assigned assets)

Page: /my-assets
Component: <TopNavbar />
Component: <MyAssetList /> - Cards showing assigned devices
Component: <AssetDetailsModal />
Component: <ReportIssueButton />

Page: /profile
Component: <TopNavbar />
Component: <ProfileDetailsCard />
Component: <ChangePasswordForm />

--------------------------------------------

Common Pages (Shared Across Roles)

Page: /login
Component: <LoginForm />
Component: <BrandLogo />

Page: /forgot-password
Component: <ForgotPasswordForm />

Page: /reset-password
Component: <ResetPasswordForm />