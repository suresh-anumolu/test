Complete Auth0 API Endpoints
1. Authentication API (User-Facing)
Base URL: https://{YOUR_DOMAIN}.auth0.com
Authorization & Token Management
EndpointMethodPurpose/authorizeGETAuthorization endpoint (OAuth 2.0/OIDC)/oauth/tokenPOSTGet access/refresh tokens/oauth/revokePOSTRevoke refresh tokens/oauth/device/codePOSTDevice authorization flow/oauth/parPOSTPushed Authorization Requests
User Information
EndpointMethodPurpose/userinfoGETGet authenticated user info/tokeninfoPOSTValidate token (deprecated)
Database Connections
EndpointMethodPurpose/dbconnections/signupPOSTUser registration/dbconnections/change_passwordPOSTPassword reset request
Passwordless Authentication
EndpointMethodPurpose/passwordless/startPOSTStart passwordless flow/passwordless/verifyPOSTVerify passwordless code
Multi-Factor Authentication
EndpointMethodPurpose/mfa/associatePOSTAssociate MFA authenticator/mfa/challengePOSTRequest MFA challenge/mfa/authenticatorsGETList available MFA factors/oauth/tokenPOSTVerify MFA (with mfa_token)
Logout
EndpointMethodPurpose/v2/logoutGETLogout from Auth0/v2/logout?federatedGETLogout from Auth0 + IdP
SAML & WS-Federation
EndpointMethodPurpose/samlp/{client_id}GET/POSTSAML protocol endpoint/wsfed/{client_id}GETWS-Federation endpoint/login/callbackPOSTSAML/WS-Fed callback/samlp/metadata/{client_id}GETSAML metadata
Well-Known Endpoints
EndpointMethodPurpose/.well-known/openid-configurationGETOIDC discovery/.well-known/jwks.jsonGETJSON Web Key Set
Back-Channel Logout
EndpointMethodPurpose/event/backchannel-logoutPOSTReceive logout notifications from IdPs

2. Management API v2 (Admin Operations)
Base URL: https://{YOUR_DOMAIN}.auth0.com/api/v2
Authentication: Bearer token with Management API scopes
Actions
EndpointMethodPurposeScopes/actions/actionsGETList actionsread:actions/actions/actionsPOSTCreate actioncreate:actions/actions/actions/{id}GETGet actionread:actions/actions/actions/{id}PATCHUpdate actionupdate:actions/actions/actions/{id}DELETEDelete actiondelete:actions/actions/actions/{id}/deployPOSTDeploy actionupdate:actions/actions/actions/{id}/testPOSTTest actionread:actions/actions/triggersGETList triggersread:actions/actions/triggers/{id}/bindingsGETGet trigger bindingsread:actions/actions/triggers/{id}/bindingsPATCHUpdate trigger bindingsupdate:actions
Applications (Clients)
EndpointMethodPurposeScopes/clientsGETList applicationsread:clients/clientsPOSTCreate applicationcreate:clients/clients/{id}GETGet applicationread:clients/clients/{id}PATCHUpdate applicationupdate:clients/clients/{id}DELETEDelete applicationdelete:clients/clients/{id}/credentialsGETGet credentialsread:client_keys/clients/{id}/credentialsPOSTCreate credentialcreate:client_keys/clients/{id}/credentials/{credentialId}DELETEDelete credentialdelete:client_keys
Connections
EndpointMethodPurposeScopes/connectionsGETList connectionsread:connections/connectionsPOSTCreate connectioncreate:connections/connections/{id}GETGet connectionread:connections/connections/{id}PATCHUpdate connectionupdate:connections/connections/{id}DELETEDelete connectiondelete:connections/connections/{id}/scim-configurationGETGet SCIM configread:connections/connections/{id}/scim-configurationPATCHUpdate SCIM configupdate:connections
Users
EndpointMethodPurposeScopes/usersGETList/search usersread:users/usersPOSTCreate usercreate:users/users/{id}GETGet user by IDread:users/users/{id}PATCHUpdate userupdate:users/users/{id}DELETEDelete userdelete:users/users/{id}/rolesGETGet user rolesread:roles/users/{id}/rolesPOSTAssign rolesupdate:users/users/{id}/rolesDELETERemove rolesupdate:users/users/{id}/permissionsGETGet user permissionsread:users/users/{id}/permissionsPOSTAssign permissionsupdate:users/users/{id}/permissionsDELETERemove permissionsupdate:users/users/{id}/organizationsGETGet user organizationsread:organizations/users/{id}/enrollmentsGETGet MFA enrollmentsread:users/users/{id}/enrollmentsDELETEDelete MFA enrollmentdelete:users/users/{id}/identitiesPOSTLink accountsupdate:users/users/{id}/identities/{provider}/{user_id}DELETEUnlink accountsupdate:users/users/{id}/authentication-methodsGETGet auth methodsread:users/users/{id}/authentication-methodsPOSTCreate auth methodcreate:users/users/{id}/authentication-methods/{authId}GETGet auth methodread:users/users/{id}/authentication-methods/{authId}PATCHUpdate auth methodupdate:users/users/{id}/authentication-methods/{authId}DELETEDelete auth methoddelete:users/users/{id}/sessionsGETGet user sessionsread:sessions/users/{id}/sessionsDELETERevoke user sessionsdelete:sessions
Roles
EndpointMethodPurposeScopes/rolesGETList rolesread:roles/rolesPOSTCreate rolecreate:roles/roles/{id}GETGet roleread:roles/roles/{id}PATCHUpdate roleupdate:roles/roles/{id}DELETEDelete roledelete:roles/roles/{id}/permissionsGETGet role permissionsread:roles/roles/{id}/permissionsPOSTAdd permissionsupdate:roles/roles/{id}/permissionsDELETERemove permissionsupdate:roles/roles/{id}/usersGETGet role usersread:roles
Organizations
EndpointMethodPurposeScopes/organizationsGETList organizationsread:organizations/organizationsPOSTCreate organizationcreate:organizations/organizations/{id}GETGet organizationread:organizations/organizations/{id}PATCHUpdate organizationupdate:organizations/organizations/{id}DELETEDelete organizationdelete:organizations/organizations/{id}/membersGETList membersread:organization_members/organizations/{id}/membersPOSTAdd memberscreate:organization_members/organizations/{id}/membersDELETERemove membersdelete:organization_members/organizations/{id}/invitationsGETList invitationsread:organization_invitations/organizations/{id}/invitationsPOSTCreate invitationcreate:organization_invitations/organizations/{id}/invitations/{invitationId}DELETEDelete invitationdelete:organization_invitations/organizations/{id}/enabled_connectionsGETGet connectionsread:organization_connections/organizations/{id}/enabled_connectionsPOSTEnable connectioncreate:organization_connections/organizations/{id}/enabled_connections/{connectionId}DELETEDisable connectiondelete:organization_connections
Resource Servers (APIs)
EndpointMethodPurposeScopes/resource-serversGETList APIsread:resource_servers/resource-serversPOSTCreate APIcreate:resource_servers/resource-servers/{id}GETGet APIread:resource_servers/resource-servers/{id}PATCHUpdate APIupdate:resource_servers/resource-servers/{id}DELETEDelete APIdelete:resource_servers
Rules (Legacy)
EndpointMethodPurposeScopes/rulesGETList rulesread:rules/rulesPOSTCreate rulecreate:rules/rules/{id}GETGet ruleread:rules/rules/{id}PATCHUpdate ruleupdate:rules/rules/{id}DELETEDelete ruledelete:rules
Logs
EndpointMethodPurposeScopes/logsGETGet logsread:logs/logs/{id}GETGet log by IDread:logs
Stats
EndpointMethodPurposeScopes/stats/active-usersGETGet active usersread:stats/stats/dailyGETGet daily statsread:stats
Tenants
EndpointMethodPurposeScopes/tenants/settingsGETGet tenant settingsread:tenant_settings/tenants/settingsPATCHUpdate tenant settingsupdate:tenant_settings
Email
EndpointMethodPurposeScopes/emails/providerGETGet email providerread:email_provider/emails/providerPOSTConfigure email providercreate:email_provider/emails/providerPATCHUpdate email providerupdate:email_provider/emails/providerDELETEDelete email providerdelete:email_provider
Guardian (MFA)
EndpointMethodPurposeScopes/guardian/factorsGETList MFA factorsread:guardian_factors/guardian/factors/{name}GETGet factorread:guardian_factors/guardian/factors/{name}PUTUpdate factorupdate:guardian_factors/guardian/enrollments/{id}GETGet enrollmentread:mfa_enrollments/guardian/enrollments/{id}DELETEDelete enrollmentdelete:mfa_enrollments
Branding
EndpointMethodPurposeScopes/brandingGETGet brandingread:branding/brandingPATCHUpdate brandingupdate:branding/branding/themes/defaultGETGet themeread:branding/branding/themes/defaultPATCHUpdate themeupdate:branding/branding/templates/universal-loginGETGet login templateread:branding/branding/templates/universal-loginPUTUpdate login templateupdate:branding/branding/templates/universal-loginDELETEDelete login templatedelete:branding
Prompts
EndpointMethodPurposeScopes/promptsGETGet promptsread:prompts/promptsPATCHUpdate promptsupdate:prompts/prompts/{prompt}/custom-text/{language}GETGet custom textread:prompts/prompts/{prompt}/custom-text/{language}PUTUpdate custom textupdate:prompts
Attack Protection
EndpointMethodPurposeScopes/attack-protection/breached-password-detectionGETGet settingsread:attack_protection/attack-protection/breached-password-detectionPATCHUpdate settingsupdate:attack_protection/attack-protection/brute-force-protectionGETGet settingsread:attack_protection/attack-protection/brute-force-protectionPATCHUpdate settingsupdate:attack_protection/attack-protection/suspicious-ip-throttlingGETGet settingsread:attack_protection/attack-protection/suspicious-ip-throttlingPATCHUpdate settingsupdate:attack_protection
User Blocks
EndpointMethodPurposeScopes/user-blocksGETGet blocksread:users/user-blocks/{id}GETGet block by IDread:users/user-blocks/{id}DELETEUnblock userdelete:users
Tickets
EndpointMethodPurposeScopes/tickets/password-changePOSTCreate password change ticketcreate:user_tickets/tickets/email-verificationPOSTCreate email verification ticketcreate:user_tickets
Jobs
EndpointMethodPurposeScopes/jobs/users-importsPOSTImport userscreate:users/jobs/{id}GETGet job statusread:users/jobs/{id}/errorsGETGet job errorsread:users/jobs/users-exportsPOSTExport usersread:users/jobs/verification-emailPOSTSend verification emailupdate:users

3. MyAccount API (User Self-Service)
Base URL: https://{YOUR_DOMAIN}.auth0.com/api/v1
EndpointMethodPurpose/users/{userId}/authentication-methodsGETList auth methods/users/{userId}/authentication-methodsPOSTAdd auth method/users/{userId}/authentication-methods/{id}GETGet auth method/users/{userId}/authentication-methods/{id}PATCHUpdate auth method/users/{userId}/authentication-methods/{id}DELETERemove auth method/users/{userId}/mfa-factorsGETList MFA factors/users/{userId}/sessionsGETList sessions

Common Query Parameters
ParameterUsageExamplepagePage number?page=0per_pageItems per page?per_page=50include_totalsInclude count?include_totals=trueqSearch query?q=email:"user@example.com"search_engineSearch version?search_engine=v3fieldsField filtering?fields=user_id,emailinclude_fieldsInclude/exclude?include_fields=truesortSort results?sort=created_at:-1

Getting Management API Token
bashcurl --request POST \
  --url https://YOUR_DOMAIN.auth0.com/oauth/token \
  --header 'content-type: application/json' \
  --data '{
    "client_id":"YOUR_M2M_CLIENT_ID",
    "client_secret":"YOUR_M2M_CLIENT_SECRET",
    "audience":"https://YOUR_DOMAIN.auth0.com/api/v2/",
    "grant_type":"client_credentials"
  }'

Quick Reference by Use Case
User Management

Create: POST /api/v2/users
Read: GET /api/v2/users/{id}
Update: PATCH /api/v2/users/{id}
Delete: DELETE /api/v2/users/{id}
Search: GET /api/v2/users?q=email:"user@example.com"

Authentication

Login: POST /oauth/token
Get user info: GET /userinfo
Logout: GET /v2/logout
MFA: POST /mfa/challenge

Password Reset

Request: POST /dbconnections/change_password
Ticket: POST /api/v2/tickets/password-change

Roles & Permissions

Assign role: POST /api/v2/users/{id}/roles
Get permissions: GET /api/v2/users/{id}/permissions


This is a comprehensive reference of 250+ Auth0 endpoints! Would you like me to:

Create examples for specific endpoints?
Explain authentication flows in detail?
Show how to use these in your RiskSpan integration?
