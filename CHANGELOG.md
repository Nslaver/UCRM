# Changelog

## 2.9.0-beta3 (2018-01-19)

### Added
*	API extended with ticketing groups management.

### Changed
*	Bank account is now hidden in the Stripe ACH payment overview.
*	"Portuguese PT" set as the default fallback language for missing "Portuguese BR" translations.

### Fixed
*	Fixed error in the manual editing of client's NetFlow data usage.
*	Fixed disappearing IMAP inbox settings when a ticket is deleted.
*	Fixed crashes when IMAP inbox settings are deleted and "Show original" or "Show attachment" is requested on a related ticket.
*	Security fixes.
*	Minor fixes.

## 2.8.2 (2018-01-19)

### Added
*	New currency TZS.

### Changed
*	Stronger SSL ciphers are now used in the built-in nginx server when UCRM HTTPS is enabled.

### Fixed
*	Search tool not giving proper results after batch import of Client CSV file.
*	All imported clients from CSV file, have all billing attributes set as "use system default" now.
*	Fixed client's email reply on "Ticket change status" notification triggering a new ticket. Now it creates a new comment in the existing ticket thread properly.
*	Fixed drag & drop feature on the Scheduling Timeline. This issue appeared in Windows only.
*	Fixed IPPay forms in browsers not supporting HTML5 validation. Causing crashes when the card num / expiration / cvv fields were sent empty.
*	Minor fixes and UI/UX improvements.
*	Security fixes.
*	API doc fixes.

## 2.9.0-beta2 (2018-01-11)

### Added
*	Now, the client's ID accompanies the client's name in every drop-down menu enabling you to choose the proper client.
*	UX Improvements, such as a link to view all client's jobs on client's profile page.
*	Translations updated.

### Fixed
*	Possibly failing upgrade to 2.9.0-beta1 in some rare cases.
*	Fixed notification for a new ticket with only attachment and no text.
*	Fixed private ticket headers visible in client zone (not the comments or attachments though) and other minor fixes for Ticketing.
*	Fixed disappearing of the Ticketing IMAP settings.
*	Errors in managing ticket attachments.
*	Minor security fixes.
*	Minor fixes.

## 2.8.1 (2018-01-11)

### Changed
*	PHP updated to version 7.1.13.

### Fixed
*	Several security fixes.
*	Possible error when editing Service Plan.
*	Failing job attachment upload for some rare mime types.
*	Fix CSV import when zero date is present.
*	Fixed Stripe ACH section being visible in client profile page and in create subscription page when ACH is disabled in the System Settings.
*	Ending a service with pending deferred change is disabled now. The planned deferred change must be removed first to avoid inconsistent service state.
*	Minor fixes

## 2.9.0-beta1 (2018-01-05)

### Added
*	Service Quotes. When creating a client's service, you can mark it as "Quoted". Then, you can create a quote (similar to invoice) and when the quote is accepted, the service will be automatically activated.
*	Client's NetFlow data usage can be manually edited. Check out the client's service NetFlow - table view.
*	New feature to create a new ticket from a client call log (manual client log entry).
*	Multiple Ticketing IMAP inboxes are configurable now. Each inbox can be associated with some User Group which is responsible for handling related tickets.
*	Check out the number at the ticket title indicating the count of new replies which you haven't read yet.
*	New filters for Ticketing. Now, you can find tickets having the latest comment created by client, i.e. tickets which probably need some attention.
*	API enhancements - IPpay payment subscription can be created in UCRM using the API.
*	UX improvements (Surcharge tax is now visible when creating a new service, etc)
*	UI/UX improvements, such as invoice pay button directly on the invoice grid, better service selection when invoicing ended or obsolete services, etc.
*	New way how to print the payment. Use the print button on the payment detail page and modify the page layout etc. on your own.
*	Notes added to UCRM payments are now editable.
*	Improved Ticketing UI in Client Zone.
*	New localizations added: Slovak, Danish.

### Changed
*	Improved Data Usage Report. Upload, download and period are now in separate columns.
*	Configuration of the login page banner moved from Organization settings to the Appearance section.
*	Service tax summary improved in the service details box. The service surcharge tax is always shown now. (Before, it was included only when the surcharge tax and the service tax were the same.)

## 2.8.0 (2018-01-05)

### Added
*	You can choose whether to use system default IDs for your clients (starting from 1) or a custom ID defined by you (starting from any number). Then, the selected ID will be shown everywhere throughout the system including the Client Zone. (Note, that all API data clients data remains to be identified be the default system ID.)

### Fixed
*	Errors in permanent deletion of client in some cases.
*	Private ticket attachments were downloadable by clients (although they were not visible).
*	Minor security fixes.
*	Improved validation for Ticketing autoreply template.
*	Fixed taxes overview in service detail and in invoice form (not all the taxes or previously removed taxes were shown in some rare cases).
*	New lines in ticket comments are well formated also in related email notifications now.
*	Email resending is now disabled in case the email log entry has no recipient defined.
*	Wrong type of template was used for ticketing notifications working (in some cases when IMAP integration is enabled).
*	State was ignored in Clients CSV import.
*	Minor fixes.

## 2.7.8 (2017-12-22)

### Fixed
*	Fixed import of Payments CSV file.

## 2.8.0-beta4 (2017-12-20)

### Fixed
*	Better results for the header search bar tool.
*	Help guide updated.
* Fixed Payments CSV import in System > Tools > CSV Import.
*	Minor UI fixes and improvements.

## 2.7.7 (2017-12-20)

### Fixed
*	Fixed permission check for several actions.
*	Fixed client's outage badge disappearing for a short while after some service was edited.
*	Fixed synchronisation of airOS traffic shaping for CPE devices.
*	Suspension page fixes. Failures when two clients have the same IP. Fixes in URL generated on the suspension page in case HTTPS is used in UCRM.
*	Creating erroneous jobs in the scheduling timeline with double-click was disabled.
*	Service IP unique check was extended to client's detached devices (detached from services). Additionally, you can search clients with IP address of these detached devices now. API validation for unique client IP was also added for creating new service device.
*	Fixed custom client attributes errors in Client CSV export.
*	Fixed service editing form in case the related service plan's period is no longer available. (Existing services can still use it, but new service can be created only with enabled service plan periods.)
*	Date picker not rendering correctly and other minor UI/UX fixes.
*	Minor fixes in service "Contract section". Now, the displayed early termination fee price corresponds with service parameters, not previously created fee.
*	Super admin account cannot be deactivated now.

## 2.8.0-beta3 (2017-12-07)

### Added
*	"US half letter" format added to PDF export options.
*	New link to client added to the invoice detail page.
*	Unknown service devices are no longer synchronized.
*	WalkMe guides added to UCRM online demo.
*	Menu shortcuts UI/UX improvements.

### Fixed
*	Fixed failing QoS setup on EdgeOS of unknown version.
*	No Ticketing search results are shown for users without appropriate permissions.
*	Minor fixes.

## 2.7.6 (2017-12-07)

### Fixed
*	Improved Client CSV validations preventing import failures.
*	Taxes associated with service were always applied to surcharges despite the defined tax of the surcharge. Now the surcharge tax (when defined) overrides the taxes of the service or the client correctly.
*	Help section is shown as the last one while using the header search bar tool.
*	Better validations and minor fixes for Stripe webhooks and Client custom attributes.
*	Possible bug with Authorize.Net post-dated payment not being imported into UCRM.
*	HTML sanitized for email templates preview.
*	More tooltips and guides improvements.
*	Belarus currency code fixed from BYR to BYN.
*	PHP upgraded to version 7.1.12.

## 2.8.0-beta2 (2017-11-20)

### Added
*	Improved Stripe ACH guides and tooltips.
*	UCRM with edgeOS v. 1.10+ is able to shape a higher number of clients now, around 16,000.

### Changed
*	Changed Elasticsearch priorities to show better results.
*	Data usage report now contains suspended services as well.
*	Organization logo and the banner is taken from the only configured organization automatically. In case there is more than one organization, it is taken from the one marked as "default".

### Fixed
*	Data usage report failing to generate in some cases.
*	Dashboard financial information toggle is persistent even after a page reload.
*	API fixes related to private tickets and other API improvements.
*	Manually terminated suspensions (caused by past due invoices) are not reactivated automatically until a new past due invoice occurs.
*	Fixed job edit when duration is empty.
*	Fixed form submit in Microsoft Edge browser.
*	Minor fixes.

## 2.7.5 (2017-11-16)

### Added
*	Improvements for CSV Import feature. Imported payment can be associated with a client. You can also use a sample CSV.

### Fixed
*	Failing service deferred change cancellation and deleting.
*	Failing emails sending in case of an invalid email address (empty string values created in an older version or through API).
*	Better results for the header search bar. (For example, results with exact invoice number match are always shown first. Client's service can be found by a note, etc.)
*	Better validations for creating a ticket with API.
*	Ticket comments created with API were always public.
*	Fixed minor bug on invoice form. (Recalculation failed when created date was not set.)
*	Minor fixes.

## 2.8.0-beta1 (2017-11-08)

### Added
*	Extended Data usage report.
*	ACH payments enabled for Stripe.
*	API enhancements: Services can be filtered by their status which may be useful to get the IPs of all suspended clients. Clients and Invoices can be filtered and sorted within the GET method. Unassigned jobs and tickets can be now filtered.
*	New features for Ticketing: Automatic reply for client's tickets created through email sent to the IMAP inbox; Option to merge unknown email address from ticket reply into client's contacts.
*	Major Ticketing UI/UX improvements. Chat style introduced.
*	Major Suspension page improvement. Clients are now enabled to pay online directly from the suspension page without entering the client-zone. Clients just click on Postpone suspension and are redirected to the payment page. No login is required.
*	Additionally, clients can reactivate their own terminated service. You can configure this in System > Settings > Client zone.
*	Added more printing page sizes for Invoice, Payment receipt and General PDF export in System Settings.
*	You can define your own shortcuts for frequently used pages, see the left-hand side panel.
*	Scheduling UI improvements.
*	As an administrator you can create private tickets now and ticket attachments are deletable now.
*	Improved header search tool, company can be found by contact name.
*	Date and time added to the new payment form.
*	A new option in service plan settings to include its instances (i.e. client's services) in FCC reports.
*	Improved client import tool for importing UCRM CSV files or any custom CSV files with multiple phones or emails in a single field separated by a comma.
*	New notification templates: for ticket comments with enabled and disabled IMAP integration. You can define ticketing email template which suits you the most.
*	You can now customize two versions of suspension page: for past due clients and for any other suspension reasons.
*	Excluded NetFlow IPs. NetFlow traffic between clients and these IPs will not be involved in the client's data usage.
*	New configuration for Client Zone and client-related features available in UCRM system settings. For example, you can enable service reactivation, suspension postponing, show more payment details, etc.
*	New settings section: Customization (formerly: Notifications) where you can configure many email templates, invoice template, suspension page, UCRM appearance, etc.
*	Custom favicon configurable in System > Customization > Appearance.
*	Client contacts enhancements. Now, for each contact, you can set a name and a default or custom type.
*	UX improvements and minor fixes.
*	Improved app performance.

### Changed
*	Attaching a file without a text to a ticket is now possible.
*	Client ID is now the primary ID used for clients (in the URL, in API, in client profile). You can still define client's Custom ID (formerly User Ident) and use both as placeholder in any notification and use it in the search bar.
*	You can define 2 date formats in system settings: "Default date format" which is used for UCRM frontend and "Alternative date format" for printed documents such as invoices and payment receipts.
*	Billing reports moved to new main menu section Reports.
*	Client list is ordered by client ID (newest first) as default.
*	An option to create a credit from an overpayment was removed from client's payment page. All invoices are paid by default in case of an overpayment created by client.
*	Client's outstanding is now shown as a positive number.
*	Subscription cancelled notification templates for each payment gateway were replaced with a single template with placeholders.
*	Better UCRM anonymous statistics, read more in in-app user guide.
*	Some docker containers removed.

### Fixed
*	Fixed creating new collection items in several forms.
*	"Recognized suspension page" is correctly shown for clients having IP range assigned to the suspended service.

## 2.7.4 (2017-11-08)

### Added
*	Translations updated.

### Fixed
*	Fixed slow dashboard loading.
*	Stripe subscription payments not matched to invoices. Instead, they were turned into client's credit in some cases.
*	Fixed termination of service suspension in some cases when a new payment is received but more than one invoice is overdue.
*	Elasticsearch index properly initialized after UCRM is restored from backup.
*	Minor fixes.

## 2.7.3 (2017-11-02)

### Added
*	More logs of device synchronization are now available on the device detail page.

### Fixed
*	Fixed issue with multiple overdue invoices with long suspension delay causing suspension not being terminated after a payment.
*	Fixed job duration in exports.
*	Fixed invalid errors with form submit with hidden elements (e.g. new job with empty task)
*	IMAP ticket with attachments not created in some rare cases and fixed attachments download for IMAP tickets.
*	Fixed device sync issues and issues with creating device backup file.
*	Fixed creating ticket comment with empty attachment file through API.

## 2.7.2 (2017-10-31)

### Added
*	UX improvements.
*	Added BDT currency.
*	Improved searching by client's ID number.

### Changed
*	API improvements for Ticketing (added filters, sort and limit options) and ticket comments refactored to activities involving both comments and ticket log entries.
*	PHP updated to version 7.1.11.

### Fixed
*	NetFlow data being labeled with wrong time in some cases when non-UTC timezone is used.
*	Postponed suspension of a service is properly canceled when a new payment is created for past due invoice.
*	Fixed searching invoices and payments by client's name.
*	Fixed crashes caused by errors during generating invoice PDF.
*	Fixed service suspension not being terminated automatically after a new payment in several cases.
*	Minor fixes

## 2.7.1 (2017-10-13)

### Changed
*	Authorize.Net payment form in UCRM no longer requires CCV code.
*	Improved server port tooltip to say SSL certificate must be set up before HTTPS can be used.

### Fixed
*	Fixed matching Stripe payments to wrong clients when they were not requested by UCRM.
*	Fixed Authorize.Net subscription creation crashing in rare case.
*	Fixed CSV import crashing without any error when item count over limit.
*	Fixed XSS vulnerability in client zone support form and in more text toggle
*	Fixed service taxes not showing in edit form when they were set up before.
*	Reworked file permissions handling at UCRM boot fixing the hanging boot problem.

## 2.7.0 (2017-10-06)
Incorporates all new features and fixes from 2.7.0-beta1 up to 2.7.0-beta4
 
## 2.7.0-beta4 (2017-10-06)

### Fixed
*	Fixed placeholder usage in the New Ticket notification for admins and other minor fixes.

## 2.7.0-beta3 (2017-10-04)

### Added
*	IMAP connection check added to the dashboard.
*	New troubleshooting guide for Unresolved host error (also related to outgoing emails failures).
*	Improved Authorize.Net guide for recurring payments.
*	You can view email original for each ticket comment sent by a client into the Ticketing IMAP inbox.
*	API enhancements for Ticketing and Scheduling.
*	Links in flash messages are now clickable.
*	Translations updated.

### Changed
*	App speed improvements, static suspension redirect page added to minimize server load.
*	Better shaping on airOS devices. Device restarts are no longer needed and device connection to UNMS is not affected.
*	When the status of a queued job is changed, the job is automatically assigned to the current user and job datetime is set to the current timestamp.
*	Recurring payments are off by default in new UCRM installations because it needs some additional paygate configuration before it's turned on in UCRM.
*	PHP updated to version 7.1.10.

### Fixed
*	IPpay payments not delivered to UCRM.
*	Fixed possible problem when UCRM boot hanged at "Initializing: Dirs".
*	Fixed deleting clients with uninvoiced fees.
*	Fixed creating tickets with attachments from IMAP integration.
*	New UCRM Installer version 1.4. Fixing issue with the permissions when the user "ucrm" already exists.
*	Fixed Service device modal window throwing error "Resource not found" when the associated network device has been deleted.
*	Fixed matching and editation of payments with "Custom" method (created via API).
*	Minor fixes and UI improvements.

## 2.7.0-beta2 (2017-09-14)

### Fixed
*	Failing MercadoPago IPN.
*	Proper data pruning for UCRM sandbox termination.
*	Fixed dashboard data permissions for the mobile app.
*	Minor fixes in the Reporting section.
*	Minor UI, UX fixes.

## 2.7.0-beta1 (2017-09-12)

### Added
*	Automatic service setup fee and early-termination fee. Configurable in System > Items > Service plans. Also, note that Service contract length was renamed to Minimum contract length.
*	IMAP Integration for Ticketing. You can bind your mailbox with the Ticketing module which will create a new ticket or ticket comment from every incoming email.
*	MercadoPago payment gateway integrated to UCRM. Now you can use many payment methods like OXXO, Boleto and many other credit, debit, and cash payments, including payment subscriptions.
*	Now, you can define taxes for service plans, products, surcharges or fees. If this tax is set, it will be always used for invoicing regardless of the taxes associated with the client. Typically, this is used in non-US countries.
*	2-factor authentication. You can enhance the app security by enabling 2-factor authentication for your UCRM user account.
*	UCRM Mobile app connectivity. Get your QR connection code from your personal account page.
*	Better web responsivity, client zone adjusted for mobile usage.
*	Major app speed improvements and better grids filtering and sorting.
*	You can enable/disable clients to postpone their service suspension by 24 hours. In System > Billing > Suspension.
*	Connection all payment gateways is checked. When an error occurs, a warning is shown on the dashboard.
*	API extensions, new payments can be automatically attached to client's invoice, payment receipt can be sent using API, user's credentials authentication, and other API extensions.
*	File attachments enabled for Tickets and Scheduled jobs.
*	Services with postponed suspension are visibly labeled and the suspension can be repeatedly postponed by the administrator.
*	Payment receipts are printable / downloadable now.
*	Improved Batch Mailing module - placeholders, UX improvements.
*	You can modify UCRM look using your own CSS. (Go to System > Tools > Custom CSS)
*	Many UI/UX Improvements, more tooltips and in-app guides.

### Changed
*	Deferred change is available even for prepared services now.
*	Assigning of administrators to a ticket is now visible in the ticket's log of communication and events.

### Fixed
*	Fixed job duration in my jobs agenda view.
*	Fixed sending empty "invoice generated" notifications.
*	Minor fixes.
*	Fixed minor security issues with uploading webroot files and restoring UCRM from a malicious backup file.
*	Client's data usage table not including data for the first or last day of the billing period in some cases.

## 2.6.2 (2017-09-05)

### Added
*	Troubleshooting guide for setting up Stripe payments.
*	Better UX for CSV and PDF exports. Empty files are not marked as a failure.
*	New currencies added: DZD, MAD.

### Changed
*	Current client email is used for Stripe payments instead of the email saved on the invoice.
*	PHP updated to version 7.1.9.

### Fixed
*	Failing client export to CSV.
*	Failing database restore in some cases.
*	Possible SMTP timeouts bug with some servers.
*	Possible problems with turning off the maintenance mode after UCRM upgrade.
*	Broken FCC Broadband Subscription report generation.
*	Fixed view permissions for some system settings pages.

## 2.6.1 (2017-08-16)

### Fixed
*	Failing Let's Encrypt tool.
*	Several form fields validations added for security reasons.
*	Better error handling while starting UCRM.
*	Failing payment adding using API in case there are more organizations with different currencies in UCRM. Additionally, the payment currency can be set. If not set, it is derived from the client's organization.

### Added

## 2.6.0 (2017-08-10)

### Added
*	New currencies added: Central and West African CFA franc.

### Fixed
*	App security extensions.

## 2.6.0-beta3 (2017-08-08)

### Added
*	Tickets can be deleted now, in a batch also. Additionally, creating tickets from the client-zone support form can be turned off in System > Settings.
*	Added SLL currency - Sierra Leonean leone.

### Changed
*	Organization name is shown instead of username in the ticket reply header in the client zone.
*	"Use credit" toggle is now shown only when creating a new invoice or editing a draft invoice.
*	PHP updated to version 7.1.8.

### Fixed
*	Periods in Data Usage table are shown correctly regardless of any changes in invoicing parameters made to a service.
*	Access denied to ticketing module even for administrators with proper access rights.
*	Buttons for edit / delete client logs not working.
*	Shaping rules synchronization not working when the description of shaping queue was modified manually on the router.
*	Device outages doubled in notification message in a specific case.
*	Service suspended falsely when deferred change is applied.
*	Failing PayPal subscription setup (appeared as of v. 2.6.0-beta1)
*	Minor security fix (Content Security Policy) added to system notifications.
*	Better search results for Elasticsearch.
*	Several minor fixes and additional validations.

## 2.6.0-beta2 (2017-07-28)

### Added
*	Payment subscriptions can be removed from UCRM even without connection to the payment gateway.
*	App speed improvements for client's detail page having many log entries.

### Changed
*	NetFlow auto setup now available only for EdgeRouters.
*	Ticket notifications are sent from the support email address now.

### Fixed
*	No shaping burst was set on airOS devices with egress only shaping.
*	Payments coming from IPpay subscriptions are labeled correctly now.
*	User-friendly notification shown when a client cannot be deleted due to an existing payment subscription.
*	Minor data adjustments when submitting Authorize.Net payment form.
*	Failing IPpay payments and subscriptions with CC expiration month in October.
*	XSS vulnerability in scheduling timeline.
*	UI fixes and improvements.

## 2.6.0-beta1 (2017-07-14)

### Added
*	Ticketing module. Ticket is automatically created when a client sends a request from the client zone. Features: keep track of the communication, assign it to an administrator, mark as solved, manage with API.
*	Bulk emailing module. You can send an email to a subset of your clients in System > Tools > Mailing.
*	Scheduling improvements. Now you can add tasks into a job which can be used as TODO list.
*	Custom clients' tags. You can create a custom tag (such as VIP or Downloader) and associate it with client. Then you can also filter clients by these tags.
*	Google calendar synchronization. Sync your UCRM jobs into your google calendar account.
*	IPpay automatic subscription payments. Administrators or clients can set up recurring payments using IPpay.
*	Shaping burst for airOS CPE devices. Define the download and upload burst for each service plan in System > Items.
*	In-app upgrade feature. As of this version, you will be notified about a new version available and you can upgrade to it using a single button. 
*	All important grids can be exported to CSV or PDF now.
*	Now you can resend any email whose sending failed. Go to client's email log or system email log.
*	New system notification settings - decide whether to send them by email or into the header notification status bar. Go to System > Notifications > Settings.
*	Notifications preview. Now you can get a preview of all system and client's notifications.
*	Now, you can upload your customized background for UCRM login screen.
*	Better client status indicators. You can now see the "invitation email pending" status until it is really sent from the email queue successfully.	
*	New placeholders now available for client notifications, for example client ID, username or client's account balance information.
*	Client zone UX improvement. Unpaid invoices are shown on the top of the client's dashboard page.
*	Initial UCRM setup wizard requires credentials now due to security reasons. These credentials are generated at the end of installation process.
*	Custom client attributes can be managed by UCRM API now.
*	More service default parameters can be defined in System > Billing.	
*	Now, you can view the log of the SSL certificate upload and setup in System > Tools > SSL Certificate.

### Changed
*	Various UX/UI improvements on the dashboard, scheduling module, etc.
*	Better confirmation messages.
*	The manual suspension is allowed only while using a custom suspension reason. "Payments overdue" reason is now applied automatically only.
*	Now, you can manually invoice a service which has been or will be modified (using the deferred change).
*	Improvements for Elasticsearch in the header bar - speed improvements and failure detection shown on the dashboard.
*	Clients export feature extended. Now all clients data including custom attributes are exported.

### Fixed
*	Fixed possible bug in the duration of separately prorated invoice periods.
*	Wrong service price - no prorating was applied when Period Start Day is set to "last" and Invoicing From is between 29th and 31th.
*	Header bar search failed for some entities, such as searching clients by IP.

## 2.5.3 (2017-07-13)

### Added
*	PHP updated to version 7.1.7.

### Fixed
*	Failing HTTPS setup with custom SSL certificate upload.

## 2.5.2 (2017-07-10)

### Added
*	Service status now available in UCRM API.
*	Added missing provinces for Canada.

### Fixed
*	Custom client attributes not shown in some cases when custom invoice template was used.
*	No taxes applied automatically when adding a late fee to an invoice manually.
*	Flag for "Separate invoicing of prorated period" was ignored in automatic recurring invoicing in some rare cases.
*	Better error handling when setting up Stripe recurring payments.

## 2.5.1 (2017-06-30)

### Fixed
*	Broken item selection in grids for exports into CSV or PDF.
*	Invoices not automatically generated on a proper day for Backward Invoicing. ("Create X days in advance" parameter ignored.)
*	These API calls fixed: GET ServiceDevice, GET ServiceSurcharge for the service and GET ServiceIp for the serviceDevice.
*	NetFlow download data fixed. UCRM auto NetFlow setup now uses "netflow enable-egress" option for NetFlow version 9.
*	Minor fixes in device outage detection and NetFlow data collecting.

## 2.5.0 (2017-06-22)

### Changed
*	PHP updated to version 7.1.6.
*	Translations updated.

### Fixed
*	Proper error handling when creating payment subscription failed for PayPal and Authorize.Net.
*	Fixed possible malfunction of automatic SSL setup using Let's Encrypt.
*	Fixed excessive automatic creation of late fees from a single overdue invoice.
*	When archiving clients their ended services' End Date is not modified now.
*	Fixed invoice sorting by due date.
*	CSRF Protection and minor fixes.
*	Fixed permissions check for job editing actions.
*	Minor UI fixes.

## 2.5.0-beta4 (2017-06-12)

### Changed
*	UX Improvements.

### Fixed
*	Fixed permanent client deletion.
*	Fixed creating invoices X days in advance for Forward Invoicing.

## 2.4.3 (2017-06-12)

### Changed
*	Maximum file size for Organization logo and stamp is now limited to 2 MB.
*	UX Improvement - services with postponed suspension are marked with a label.

### Fixed
*	Fixed suspension of service IPs with a netmask on Mikrotik devices.
*	Repeated suspension postponing by a client is forbidden again. This feature is possible only once per each suspension.
*	Fixed permission issue when changing own password.
*	Blocking a prepared service till the activation date not working for services after reactivation.
*	CSRF protection for document uploads.
*	Other minor fixes.

## 2.5.0-beta3 (2017-06-05)

### Fixed
*	Fixed suspension synchronization.
*	Fixed client permanent delete.
*	Minor UI fixes.

## 2.5.0-beta2 (2017-06-02)

### Changed
*	Minor scheduling UX improvements.

### Fixed
*	Fix Top Downloaders filter.
*	Fixed growing chart in Safari.
*	Minor fixes.

## 2.4.2 (2017-06-02)

### Fixed
*	Fix credit being duplicated after it's used to pay for invoice. All payments are checked and if the credit was created wrongly, it will be removed from the invoice. Make sure to check your invoices after updating. Only payments / invoices created after version 2.3.0-beta1 could be affected by this bug.
*	Fixed walled garden postpone suspension button not working after it was used for previous suspension.

## 2.5.0-beta1 (2017-05-31)

### Added
*	New Scheduling Module. Create a job, monitor its life-cycle, assign it to an administrator. Additionally, all jobs can be exported and linked to your own calendar (iCal) or managed by UCRM API.
*	Antiflood and Throttler for UCRM mailer. You can turn on these new features to accommodate the needs of your mail server.
*	Custom Client Attributes. You can create a custom attribute and associate it to a client. You can also modify the invoice template to include that attribute.
*	Courtesy credit. You can create courtesy credit for a client. This works as any other payment, which increases client's credit but this credit cannot be refunded.
*	UCRM translations per administrator. Each administrator can set up his own language in the user profile. This will affect the user's view while the app localization remains applied to invoicing and client zone (still configurable in System > Settings > Localization).
*	IPpay one-time payments integrated into UCRM.
*	New placeholders are now available in custom invoice template. For example client's account standing or credit can be added to the invoice now.
*	Late fees can be configured separately regardless of the suspension feature being active. You can also define the delay which will determine when the late fee will be applied after the due date.
*	Top downloaders list. View all NetFlow data for all the clients. See Dashboard > Top downloaders > Show all clients.
*	Added Data Usage overview in a grid on client's service page. The usage is organized according to the service periods. This can be used for manual data usage billing.
*	Minimum unpaid amount to trigger suspension. Now, you can define the minimum unpaid amount of an overdue invoice to trigger the suspension. See System > Billing > Suspension.
*	You can restore a database backup in the UCRM wizard. No need to initialize whole UCRM before restoring a backup.
*	UCRM API enhancements. Now, you can create new taxes and also apply tax to an invoice item. Additionally, you can manage client's log using the API.
*	Hungarian translation added (still incomplete, translation is in progress).
*	Fancy UX improvements.

### Changed
*	The size of organization logo thumbnail in invoice templates is changed from 260x80px to 200x200px, to correspond with size of organization stamp thumbnail. Additionally you can use new invoice template variable to use original image size for both logo and stamp.
*	Better UX for client log. Now all messages are merged into a single grid giving you a better overview.
*	While a service is suspended for a whole billing period, this period is not invoiced if "Stop invoicing for suspended services" is true. All other periods even partially suspended will be invoiced as usual. Note that this option is irrelevant for prepaid services, i.e. forward invoicing.
*	For security reasons, the mail server password must be provided each time the mailer parameters are edited.
*	Suspension and Late fee features are turned off by default for new UCRM installations.

### Fixed
*	Count of Device outages shown on dashboard now complies with the default grid filters used in Network > Outages section.
*	Minor fixes related to deferred services.

## 2.4.1 (2017-05-30)

### Fixed
*	Postpone suspension button not working on client's suspension (walled garden) page. 

## 2.4.0 (2017-05-25)

### Fixed
*	Failing to mark all header notifications as read.
*	Grid sorting errors, various form validations and other minor fixes.
*	Failing Authorize.Net subscriptions due to a long client name.
*	XSS Vulnerability fixed.
*	UX fixes and improvements.

## 2.4.0-beta2 (2017-05-16)

### Added
*	New filter for device outages grid. Now, you can filter out all the outages of devices with turned off outage notifications.
*	SZL (Swazi Lilangeni) currency added.

### Changed
*	When client postpones the suspension, the suspension will be reactivated after 24 hours (before, it was reactivated after the today's midnight).
*	Higher contrast added for input fields to improve user experience when UCRM is used outside under the sun.
*	PHP upgraded to v. 7.1.5.

### Fixed
*	Fixed getting all VLAN interfaces and advanced information from airOS devices.
*	Fixed wrong timezone being used giving wrong results for several actions and views. Now the proper timezone of your UCRM is always used.
*	Added CSRF protection.
*	Minor fixes.

## 2.3.3 (2017-05-16)

### Fixed
*	Suspension not working and suspension notification repeatedly sent every hour. This might happen after the "Demo mode" has been terminated.

## 2.4.0-beta1 (2017-05-03)

### Added
*	Added fully automated HTTPS setup. Now, you can set up SSL certificates using Let's Encrypt. UCRM will automatically handle everything for you, including certificate renewal.
*	New Client Documents module added. You can upload any document related to your client, such as contracts, images, PDF files, etc.
*	FCC 477 Reporting. Two CSV exports (Fixed Broadband Deployment, Fixed Broadband Subscription) are available in System > Tools > FCC Reports
*	Tax inclusive pricing. Now, you can define service or product prices with tax included. You can switch to this pricing mode in System > Billing or in the initial setup wizard.
*	Added device management IP. Now, you can provide a CPE or any other device of your network with a management IP. Then, this IP will be used for all UCRM connections to the device (sync, outage detection and signal statistics) while the suspension will normally be applied to standard IP(s) of the CPE device.
*	Now, you can search client, invoice, device or site by their notes. (In the header search bar)
*	Now, the "new drafts created" notification contains a brief overview of the invoices with a link to each of them. If you have already modified the content of this notification, you can add this overview manually in System > Notifications settings.
*	Date, when the next recurring invoice will be generated, is shown on service view page.
*	UCRM backup extended. Now you can define whether to backup also important files and documents along with the whole database. (System > Tools > Backup)
*	On device view page, IP addresses and notes are now included in interface list.
*	Now, there are two types of "new invoice" notifications for administrators - for drafts and for auto-approved invoices. You can customize both or even turn them off (in System > Notifications > Settings).
*	NetFlow graphs refresh interval can be set up in System > Settings > Netflow
*	UCRM API improvements, you can edit client's services and invoices. You can also get invoice templates stored in UCRM.
*	All notifications and emails can be turned on / off in System > Notifications > Settings. You can even suppress invoice sending.
*	You can now define the minimal data traffic for "NetFlow unknown device" detection.
*	Decimal and thousand separators can be defined in System > Settings > Localization
*	CSRF protection for several pages.
*	Notification about new UCRM version added to header toolbar.
*	UX Improvements and minor fixes

### Changed
*	Invoice rounding mode "Precise non-rounded item totals" is deprecated now. It was used as a temporary workaround for determining the final service price with tax included. Now, we strongly recommend switching to the new Pricing Mode called "tax inclusive pricing".
*	Exports of Billing reports are now generated in the background. When finished, you can download it in System > Tools > Downloads
*	Service surcharge price can be left empty. Then, the default system surcharge price will be used. If left empty, the price will be updated on each service when system default is changed.
*	Changing payment currency is now allowed when matching it with an invoice.
*	While terminating Demo mode, all files are deleted now (when factory reset mode is chosen).
*	Improvements of NetFlow auto-setup for EdgeRouters. NetFlow v.9 and memory table disabling are set by default to improve the router performance.
*	Invoice discount validation improved, now only 0-100% is a valid invoice discount.
*	UCRM Translations updated.

### Fixed
*	Excessive restarts of CPE devices are eliminated. Shaper rules are now applied only when qos-related parameters are changed.
*	Now, device status is detected also before the first synchronization is done.
*	"Last successful synchronization" of a device now really shows the date of last successful sync and not the last sync attempt.

## 2.3.2 (2017-05-02)

### Fixed
*	Possibly invalid invoice numbers are fixed before invoice PDF is created.
*	Proper taxed amount rounding on "service show page" is applied in the same way as on an invoice.
*	Fixed Stripe payment issue with invalid parameters.
*	Minor bug fixes.

## 2.3.1 (2017-04-26)

### Added
*	Client ID can be added to the invoice template using the new placeholder "client.userIdent".

### Fixed
*	Better escaping of possibly harmful strings in CSV exports.
*	Fixed QoS rules synchronization on airOS devices in case service plan speed values are removed.

## 2.3.0 (2017-04-21)

### Changed
*	Escaping of possibly harmful strings in csv exports.

### Fixed
*	Fixed discount rounding to decimal places allowed by the currency.
*	Fixed PayPal payment failures for amounts greater than $999.
*	UCRM API fixed. When getting invoices or payments using date range limit, the end date is now included to the filter.
*	Elasticsearch failures when found entities have just been deleted.
*	Invoice maturity days must not be a negative number now.
*	Possible privilege escalation in the client impersonation feature.
*	Form submit button not working in Microsoft Edge and Internet Explorer browsers.

## 2.3.0-beta4 (2017-04-11)

### Fixed
*	Wrong total untaxed amount in billing reports.
*	Missing edit button added for drafts in the invoice grid.
*	Removed false client's credit entries if they possibly still exist after a related payment is unmatched from client.
*	Fixed possible failures of RouterOS device sync due to wrong SSID format.

## 2.3.0-beta3 (2017-04-07)

### Changed
*	Invoice item quantity is now shown along with the unit label such as "pcs", "meters", etc.
*	Flash message is shown when the Elastic search fails for any reason.
*	Guide for Stripe settings updated to accommodate new Stripe dashboard.
*	UCRM system logging improved (unimportant ping notices are ignored).

### Fixed
*	Crashes when exporting large billing reports (memory limits increased).
*	QoS not being updated when service changed (when service plan upgraded / downgraded to another one).
*	Price of service surcharge could not be set to $0.
*	Integer numbers were not allowed in UCRM API along with float numbers. For example: both formats $10 and $10.00 are now valid.
*	False positive alert in header notifications. In some cases, new notification sign was shown even when there was no new notification.
*	Translations fixes and updates.

## 2.3.0-beta2 (2017-03-31)

### Added
*	Papua New Guinean kina currency added.

### Changed
*	Surcharge invoice label improved. When not defined per service, global surcharge label will be used.
*	Additionally, "name" attribute of service surcharge has been removed from UCRM API.

### Fixed
*	Fixed failures in modal window for editing a service which has been terminated. 
*	Fixed error when deleting payment subscription which has been already removed from Authorize.Net.
*	Fixed crashes when generating too large billing report.
*	Translations update and fixes, better word wrapping on several places.
*	Fixed translations usage in "new invoice" email. Change of UCRM language setting is applied properly in all email notifications.

## 2.2.3 (2017-03-30)

### Fixed
*	Fixed invoice creating with empty surcharge label.
*	Fixed import of airCRM database having email duplicates.
*	Fixed discount rounding. Now, when a service with discount is invoiced manually, the negative amount of discount is rounded in the same way as all other positive numbers on the invoice.
*	Fixed bug when creating an unattached payment with undefined currency.
*	Fixed date time of device outage due to the wrong time zone used. Only new entries will be fixed.
*	Fixed form for creating a new refund.

## 2.3.0-beta1 (2017-03-23)

### Added
*	Customizable invoice templates.
*	Added deferred service change. You can define a service change to be applied on the specified date. The service will be invoiced according to the current parameters till this date (excluding this day). The changes will be applied for the next period starting on this day (including this day).
*	You can reactivate a terminated service (click on the service status label) and while doing so you can also modify any service parameters, e.g. change the billing attributes completely. 
*	UCRM translations added for Spanish, Catalan, Swedish, Turkish, Dutch, Latvian, German, Portuguese and Portuguese (Brazil). Change the UCRM language in System > Settings > Localization.
*	When deleting a client's service you can preserve the service device and attach it later to any other client's service. No need to define the device parameters again.
*	You can automatically send notifications before an invoice gets overdue. Define how many days before the invoice maturity day the notification should be sent - See System > Billing.
*	Server disk space utilization shown on the dashboard. This should prevent from crashes due to running out of free space.
*	Added HTTPS support when UCRM is deployed on a cloud with load balancer. More details and guide here: https://help.ubnt.com/hc/en-us/articles/236007047-UCRM-Install-UCRM-Cloud-using-DigitalOcean
*	You can view device password and you can allow this feature for other UCRM users in special permissions.
*	You can define the default period start day for all new services - System > Billing. You can set a fixed day e.g. 1st day in month or a current day.
*	Now you can manually change address and all other attributes on invoice - choose an invoice and click edit button.
*	System notifications added to the header. You will be notified about files being ready to download or about important errors, warnings.
*	All system logs (prod.log, nginx.log, etc) and all docker logs are compressed daily and the backups are pruned after 14 days.
*	UX improvements in service form.
*	Better UCRM booting log.

### Changed
*	Now, late fee is created for each overdue invoice even when they are related to the same service.
*	Simplified and less restricted invoicing. Now, you are enabled to create an invoice with any billing period even already invoiced. You can also delete any invoice, not only the last one in the row.
*	Less restricted custom payment subscriptions. You or your client can create a subscription at any time and with any amount. The subscription is no longer linked to a service. You can create the subscription for a client directly from the administrator's interface without a need to switch to the client-zone.
*	Now, you are enabled to delete a service having some invoices. Additionally, you can decide whether to keep them or delete them as well.
*	Invoice item quantity is rounded to 6 decimal places now.
*	Invoice subtotal is always shown with the currency symbol. When it is possible, the symbol is also used for each invoice item total.
*	Manual draft approving improved. All invoices are created in the background now.
*	Improvements of recurring invoicing. Services with different periods can be invoiced together (on condition "invoice separately" flag is set to false).
*	Backend maintenance scripts are executed more often. As a consequence, various notifications and status updates are executed earlier.
*	UI improvement - items in price summary overview are shown as links so that you can click on them and edit them, e.g. surcharge, discount or the service itself.
*	Company name is shown in header of client zone when a client of type "Company" is logged in.
*	Editing ActiveFrom date of an active service is no longer possible.
*	Update script improved. All config files are validated now.

### Fixed
*	Invoice is properly created when a service is still "Prepared" and you use forward invoicing.
*	UCRM domain name or server IP is required when outgoing emails are used in UCRM.
*	You are now enabled to set service individual price same as the plan price. This will make the service price fixed even when the plan price is changed in the future.
*	UI fixes and improvements.
*	Minor fixes and improvements.

## 2.2.2 (2017-03-22)

### Changed
*	Map in client zone is hidden now when app keys are not set.

### Fixed
*	Fixed "egress-only" shaping on AirOS v8.
*	Fixed blocked IPs synchronization on RouterOS when the synchronized IP is already blocked manually.

## 2.2.2-beta5 (2017-03-20)

### Changed
*	Payment currency validation added for manual payment matching with an invoice.

### Fixed
*	Fixed transparent background of downloaded charts.
*	Fixed restoring encryption key from UCRM backup when restoring on fresh installation.
*	On linux kernels lower than 3.17 - fixed various crashes and failures to login into UCRM (PHP 7.1.3 incorporated)

## 2.2.2-beta4 (2017-03-13)

### Fixed
*	Fixed failing PayPal payments due to wrong TLS 1.2 support.

## 2.2.2-beta3 (2017-03-10)

### Added
*	UX Improvements: grid sorting persists per each UCRM user, company website is clickable, etc.
*	URLs in email notifications are now clickable.

### Changed
*	"Tax rounding" parameter renamed to "Invoice rounding" in System > Billing > Invoicing. There are two options: "Standard rounding", which is default and recommended and "Precise non-rounded invoice item totals" which should be used only if you need to fix the service price with tax included. Note that this option has some limitations, see the in-app help for more details.

### Fixed
*	Fixed NetFlow monitoring after UCRM update. UDP item in conntrack table is purged using new update script.
*	Fixed creating new client while no default organization is defined.
*	Fixed overview of Billing reports.
*	Fixed unknown device count on dashboard.
*	Fixed synchronization of RouterOS VLAN interfaces.
*	Fixed deleting of archived clients.
*	When service is deleted, related shaper rules are removed too.
*	Fixed "NetFlow unknown device" entries when its IP matches the device interface primary IP.
*	Fix unwanted auto-fill of form fields.
*	Fixed CSV import in non-UTF-8 encoding.
*	Minor bug fixes.

## 2.2.2-beta2 (2017-02-23)

### Added
*	UCRM API upgraded with new getters (of collections and single entities too) and new filters for Invoice getter. You can filter Invoices or Payments by the Create date. Please refer to [API documentation for UCRM beta](http://docs.ucrmbeta.apiary.io).
*	Additionally, more attributes of Invoice and Payment can be retrieved using API, for example: invoice status, due date, etc.
*	Enormous app speed improvement.

### Changed
*	Added Canadian provinces into the "States" select-box.
*	PHP updated to v. 7.1.2.

### Fixed
*	Fixed detection of unknown devices connected to airOS network device (the false positives will disappear from the table after a week).
*	Fixed data synchronization for some types of Mikrotik devices.
*	Fixed crashes due to missing indexes of Elasticsearch. Now Elasticsearch data and indexes are persisted in `/home/ucrm/data`.
*	Fixed count of unknown NetFlow devices.
*	Fixed postponing the service suspension and the modal form for postponing always shows tomorrow at least. 
*	Minor fixes and UX improvements.

## 2.2.2-beta1 (2017-02-13)

### Added
*	Introducing robust client contacts management. You can assign an unlimited number of client's contacts with email and phone. Also, you can specify the purpose for each email address, e.g. different email for billing vs. general notifications.
*	And you can import clients with multiple contacts information using UCRM API and CSV import tool.
*	You can also decide whether the client's email should be used as the client-zone username or not.
*	While creating a new service with deferred activation date, you can decide whether to block the service device IP until the service is active.
*	Tax rounding option. You can choose whether to round the taxed amount for the sum of the invoice items (default) or per each invoice item.
*	Better rounding support. Item prices can be defined with up to 6 decimal places while the final invoice item totals and invoice totals are rounded according to the currency decimal limit, e.g. 2 for US dollar.
*	More formatting options added to WYSIWYG editors. For example, you can set font, color or edit the HTML source.
*	Now, you will see all the spool emails immediately in the mailer log. All emails waiting in the queue are shown with flag "E-mail in queue".
*	Emails sent while the demo mode is active are visibly marked in the mailer log.
*	You can set or change the password of your client.
*	Better error message in case the encryption key is missing in the system.
*	Warning shown when trying to assign a range of IPs to the client service because typically, a single IP is assigned to the service.
*	New system settings section Localization - to set system language, timezone, date and time format.
*	State is now loaded to new client form address from default organization as well.
*	App performance improved.
*	You can set logs expiration in system settings.

### Changed
*	You can set default invoicing attributes such as Suspend Delay in system settings. Then, this value will be used globally unless overridden in client's edit page.
*	Now, invoice overdue notifications are sent before the Suspension notification email.
*	NetFlow traffic lower than 1 MB will no longer appear in Unknown devices. E.g. if you just ping non-existing IP, it will not show up in the Unknown device list.
*	Better handling of Stripe webhook failures.
*	By default, invoice label of the service plan is used in the invoice instead of the service name. But you can override this label manually per each service if you want.
*	UX improved for editing network device.
*	Now 6 decimal places are allowed for invoice item quantity.

### Fixed
*	Fixed Client ID auto increment when there is more than one organization in UCRM.
*	Word wrapping fixed in invoice PDF.
*	XSS vulnerability fixed for CSV imports.
*	The process of generating recurring invoices starts exactly at the hour specified in system settings.
*	When clients are archived, their "outage" or "suspend" status is properly removed.
*	Fixed service surcharge order to be the same everywhere.
*	Fixed taxable values in products and surcharges grid.
*	Fixed and improved detection of unknown devices connected to airOS / RouterOS devices.
*	Fixed Authorize.Net duplicate subscription error.

## 2.2.1 (2017-01-24)

### Added
* You can now use wildcards in the search box (* to replace zero and more characters and ? to replace a single character) and boolean operators (+ to indicate the word must be present and - to indicate the word must not be present).
*	Vanuatu Vatu currency added.

### Changed
*	All primary IPs of network devices are excluded from the Unknown Devices overview.
*	Currency columns aligned to right.

### Fixed
*	Fixed reversed upload / download speed values for "egress only" traffic shaping on AirOs devices.
*	Fixed crash after restoring database backup.
*	Fix GPS latitude / longitude scale.
*	Deleted Products and Sites are no longer visible in select boxes.
*	Fixed word wrapping of invoice labels.
*	Fixed timezone detection in the UCRM init wizard.
*	Fixed EdgeOs synchronization errors (including VLAN interface discovery).
*	Fixed manual service suspension with custom "stop reason".
*	Fixed crashes when resetting filters for some grids (such as resetting date filter for client's invoice grid).
*	Fixed missing phone in CSV import of clients.
*	The attempt to setup traffic shaping on AirOs device when no download / upload speed is set is now logged properly.
*	Stripe payments now fail gracefully when there is an error (e.g. when attempting to pay less then 50 cents).
*	Fixed device links in outage notification emails when HTTPS is enabled (note that the UCRM server port must be set to 443 in system settings).
*	Fixed searching by IPs of devices and CPEs and generally improved searching
*	Minor bug fixes and UI fixes

## 2.2.0 (2017-01-13)

### Added
*	New search bar added, accessible also with "/" slash keyboard shortcut. You can find clients, invoices, payments and even help articles using a key word such as client ID, email, IP address, invoice number, etc.
*	You can also search archived clients by name, address, service IP, etc.
* UCRM Dashboard redesigned, the most important information about billing and network added.
*	While setting up HTTPS, you can now upload the CA bundle file along with your cert file.
*	Information about client's payment subscriptions are shown in client detail page.
*	API enhanced. You can retrieve all clients and all services or get entities by their ID.
*	You can manually create and download up-to-date database backup (in System > Tools).
*	Old device backup files are pruned. Last 14 backups are kept in UCRM after each synchronization.

### Changed
*	Now, you can define tax value with up to 4 decimal digits.
*	SNMP community string limited to 32 chars.

### Fixed
*	Mailer spool fixed in case there is a mail pending with invoice PDF previously removed.
*	Fixed possible bug with connection to Elastic container after UCRM update.
*	Synchronization with older EdgeOs devices improved.
*	Client sorting by ID fixed.
*	Fixed automated NetFlow set up. (For some devices, the NetFlow could have remained in pending state.)
*	Minor bugs fixed.

## 2.1.12 (2017-01-04)

### Added
*	IP of terminated service is blocked on the router
*	UCRM update process improved. In case of a failure the previous version is restored.
*	Demo-mode termination improved. You can now mark all clients as not invited and all existing invoices as not sent while terminating the demo-mode.
*	While adding a new service, you will see a warning that prorating will be applied (to prevent situation when "period start day" does not match with "invoicing start" by mistake)
*	Period start day is shown on service detail page
*	Better price and quantity validation added to the new invoice form (you can use both . and , as the decimal separator)
*	UCRM API improved. When adding a new payment, it can be matched with multiple invoices.
*	UI improvements

### Changed
*	Settings structure simplified. Main settings can be found in System > Settings. All billing parameters can be found together under System > Billing. Service plans, products and surcharges are moved under System > Items, etc.
*	DB backup simplified. You don't need to move the crypto.key while backuping or restoring UCRM database.
*	Prepared service cannot be suspended or terminated, related buttons are hidden now.
*	Invoices of archived clients are visible in the global invoice list.
*	Special permission "View financial information" affects client's financial overview and also financial overview on Dashboard now
*	Client IP not shown on walled garden suspend page unless stated explicitly using client IP placeholder in notification settings
*	Support email is shown in client-zone instead of organization email when available

### Fixed
*	Fixed outgoing invoice emails for recurring invoices (some smtp servers affected)
*	Bugs regarding invoice preview fixed in new service form
*	Default client's taxes are properly applied when creating a new invoice
*	All the client's services are shown in client zone (only the first 5 services were shown before)
*	$0 individual service price can be set now
*	Fixed inconvenient issues when user has insufficient permissions
*	PayPal error is handled properly and logged
*	Fixed minor bugs

## 2.1.11 (2016-12-16)

### Fixed
*	Fixed shaping on AirOs devices
*	When shaping is turned off on EdgeOs devices or globally in system settings, UCRM will not even connect to any EdgeOs
*	Client and service status are updated immediately after any change
*	Fixed possible bug with resolving gps coordinates
*	While creating a new invoice manually, late fees select box shows only those items which belongs to the given client
*	Minor UI, UX fixes and app speed improvements

## 2.1.10 (2016-12-14)

### Added
*	Client suspended badge added to the clients grid
*	Grids page size is remembered
*	Now, you can search invoices by their number
*	You can set default invoice note (comment) at organization > billing options. This note will be automatically added to every new invoice.

### Changed
*	Association of suspend, overdue and outage badges to clients / services is no longer pushed to system log
*	Good news for those who need custom bank account number. You can use just the first field, the second field can be left empty and no slash will be displayed.
*	Credit is now applied to an invoice in proper order (payments associated to the invoice are used from oldest to newest)

### Fixed
*	Fixed item counts and pagination for some grids
*	UI fixes for Safari browser
*	Invoice number generator fixed when non-numeric prefixes are used
*	Shaping fixed on some EdgeRouters which already used own shaping rules
* Fixed log entries for mailer errors
* Minor UI / UX fixes and improvements

## 2.1.9 (2016-12-12)

### Added
#### UX & redesign
*	Major UI, UX improvements. Mostly for client, service detail and all grids.
*	You can now filter and export clients and invoices into csv file.
*	Status tags in clients and invoices grid. At first sight, you will see an outage or overdue status at your client or invoice.
*	Now, you can search clients by their service device IP and also search network device by its IP
*	You can filter overdue invoices now

#### Shaping
*	Shaping enabled on EdgeRouters
*	If you are used to shape on your gateway router only, you can simply turn this feature on, applied to all the clients globally - in system settings.
*	If shaping on AirOs CPE devices you can choose whether to shape egress only (on wlan and lan) or egress, ingress (on wlan)

#### Other
*	Now you can specify a check number when creating a new check payment
*	More details about incoming payment from paygates are now provided in payment detail page
*	Client is enabled to modify the amount to be paid when paying online and decide to associate it with multiple invoices or to turn it into credit.
*	As a WISP, when creating a new payment you can associate it with multiple invoices
*	API upgraded - you can upload a payment with a third party paygate information.
*	GPS address is automatically resolved when creating a new service according to the client location

### Changed
*	Improved grids, filtering and related action buttons
*	Better email queue handling and error monitoring
*	Same invoice number can be used within more UCRM organizations.
*	"Quick add device" feature improved. No fictive interface is created after the first device synchronization.
*	Service taxable flag removed, since it is redundant. When some tax is associated with the service it is taxable by default
*	Major app speed improvements
*	PHP updated to v. 7.0.14

### Fixed
*	Fixed bug when tariff period being updated with empty price
*	Options for service periods rendered properly in edit service form, only valid periods related to a given service plan are shown now.
*	Fixed rendering of invoice pdf with organization logo and stamp
*	Now, the value of client's invoice maturity days overrides properly the global value set in system settings.
*	Fixed problem with outgoing outage notifications (occurred on some smtp servers)
*	Fixed possible problems with editing taxes or periods on a service
*	Now, client's taxes are automatically applied to "product" invoice item
*	$0 balanced invoices of all kinds are not sent if defined so in system settings
*	Fixed matching of subscription payments with the invoice. Some payments from paygates were marked as unmatched although it was possible to match them with an invoice automatically
*	Minor fixes and improvements

## 2.1.8 (2016-11-24)

### Changed
*	Proper paypal exception hadnling, user is notified to contact the ISP to solve the problem.
*	PHP bumped to v7.0.13

### Fixed
*	Fixed RouterOs synchronization
*	Suspended service's IPs are correctly propageted to BLOCKED_USERS list even when the service is connected to a device with disabled suspension feature
*	IPs list on interface properly synchronized. Multiple duplacate IPs are not longer created during the sync.
*	Fixed possible bug with applying client's credit to invoice.
*	Fixed outgoing notification emails in case of reapeated outages.
*	Fixed turning off the outage notification feature in system settings

## 2.1.7 (2016-11-09)

### Added
* UCRM API - new api for payments and invoices. You can upload new payments of any source and an invoice with simplified items

### Changed
* UCRM API improved - client's service entity now contains info about service plan and shaping speed

### Fixed
* Payment subscribe button shown properly in client zone (even for invioces with surcharges and taxes)


## 2.1.6 (2016-11-08)

### Fixed

*	Payment subscribe button shown properly in client zone
*	Invoices Batch print and Export button works now
*	"Drafts created" notification sent only when there is at least one new invoice
*	Disappearing menu items on some subpages fixed
*	Minor fixes for sync feature and authorize.net subscribtions handling

### Changed
*	Invoice preview (in new service form) shows total price including tax
*	While device sync, its interfaces types are set according to real interface type (wlan, ethernet, etc.)
*	Improved stability for restoring db backup

## 2.1.5 (2016-11-04)

### Added
*	UCRM API - this will enable you to mass-upload clients, services and some other main entities into UCRM. See more at http://docs.ucrm.apiary.io/
*	Subscribtions for recurring payments on Authorize.Net now available
*	EdgeOs vlan interfaces are automatically created and synchronized now
*	Filter payments by amount or client's name, email, etc.
*	You can upload file into webroot directory using UCRM interface in Settings > Tools > Webroot
*	UCRM Maintenance page shown when db backup is being restored
*	Kenyan shillings added to currency list

### Changed
*	Safe upgrade. When database migration fails during the update it is reverted to the previous state and the UCRM version is not upgraded.
*	Shaping on AirOs now accept float values. You can set up 4.25 Mbps
*	Better interface for netflow turns on/off on EdgeRouters
*	Better tooltips for sites and services on maps
*	UI performance improved

### Fixed
*	Free service plans (with billing period for 0$) can be created now
*	0$ invoice status fixed to be paid
*	Zero price in service is allowed
*	Fixed service next invoicing day shown in client zone
*	Fixed possible problem with matching / unmatching payment to invoice
*	Fixed default submit button in grid fiters
*	Problem with AirCRM data import fixed
*	Possible problem with searching fixed
*	Device synchronization logs are now displayed in correct order
*	Automatic change of server ports after activating HTTPS is now working correctly
*	When encryption key is incorrect after database restore, you should now still be able to access web interface

## 2.1.4 (2016-10-19)

### Changed
* PHP updated to v7.0.12

### Fixed
* Fixed EdgeOS connection problem with socket script upload.
* Fixed failing migration at container start.
* Fixed bug with credit being applied incorrectly after invoice was voided.
* Fixed missing validation of notification template subject.
* Fixed wrong input type for frequency on device interface form.
* Fixed wrong application help permissions (only worked for super admin, instead of all admins).
* Fixed searching in device list.
* Fixed a bug in IP validation preventing creation of service device IP.
* Fixed wrong redirect after payment was deleted on clients billing screen.
* Fixed logging of changes after device synchronization.
* Fixed a bug in AirOS device synchronization.

## 2.1.3 (2016-10-17)

### Fixed
* Fixed QoS (traffic shaping) synchronization for AirOS CPEs.
* Fixed marking devices offline after automatic addition of device interfaces.
* Fixed SSH port getting overwritten on device edit page.
* Fixed amount of synchronization log entries.
* Fixed synchronization not happening immediatelly when needed.
* Fixed errors around soft deleted entities.
* Fixed couple of UI errors.

## 2.1.2 (2016-10-11)

### Fixed
* Fixed payment rounding error. (Fixes partially paid invoices, which should be marked as paid.)
* Fixed automatic sending of invoices.
* Fixed possible problem with cache after UCRM update.

## 2.1.1 (2016-10-07)

### Added
* Encryption key donwload feature added in Settings > Tools > Database backup. Note that while migrating a new server or to reinstalled UCRM instance, you must always migrate db along with the encryption key or all the passwords stored in the db will be unreadable.
* Interfaces of type "Bridge" are now created automatically when device is synchronized

### Changed
* You can hide unsuccessful NetFlow setup tries in System Settings
* While synchronization, UCRM tries to connect to a device with only one accessible IP (if there are more accessible IPs on a device, the last successful is used. The inaccessible IPs are skipped by default. Make sure each device as at least one accessible IP)
* Setting up NetFlow is disabled until the UCRM Server IP is properly set (in Settings > General > System > Application)
* App integrated help guide improved

### Fixed
* Possible migration failure fixed (followed by crashes of multiple pages)
* Invoice numbers auto increment fixed
* Excesive log entries fixed in case of unsuccessful NetFlow setup
* Synchronization of device interfaces fixed (non existing interfaces which don't match with any real device interface are removed). See more about the matching rules in the app guide.
* Fixed crashes when trying to delete late fee which has been already invoiced
* Fixed crashes when removing Device, ServiceDevice or User with existing log entries or statistics
* Fixed validations in invoice form
* Other minor fixes

## 2.1.0 (2016-09-30)

### Added
#### Network features
* NetFlow - view download and upload data traffic of your clients
* Device synchronization - device attributes such as interfaces, IPs and many more are now automatically and periodically updated according to the physical device configuration (for EdgeOs, AirOs, RouterOs devices)
* Quick autoload af a device - whenever you need to add new device to UCRM, just provide IP, username and password and UCRM will automatically set up other attributes for you, e.g. interfaces and IPs (for EdgeOs, AirOs, RouterOs devices)
* Device statistics - you can monitor the state of your devices thanks to new charts for Signal, CCQ, Rx and Tx rates, ping latency and loss rate (for AirOs, EdgeOs, RouterOs devices)
* Device outages - view device outages log and define who and when should be notified in case of an outage (for all vendors and models)
* QoS - set up the traffic shaping (current implementation: shaping on AirOs CPE devices is now available)
* View of unknown connected devices as an outcome of netflow and synchronization features. Devices which don't belong to any client but they are connected to routers or have upload/download traffic are now detected.
#### App features
* Organization logo and site name is now shown on login page. Additionally, the site name is shown in the client-zone page headers
* Now you have full control of your client registration status. These are possible values: Not invited, Invited on.., Registered on..
* Google maps and Google geocoding are now supported. Follow the setup guide in UCRM system settings.
* SMTP setup added to the initial setup wizard
* Now, you can upload and restore a database backup of any previous UCRM version
* An overview of invoices to be send is now displayed when clicked on batch invoice sending
* Now, you can search sites and devices by names (including partial name), addresses, vendors or model names
* Application-wide help and guides are now available - click on ? sign
* Various form field validations added

### Changed
* Suspension feature can be enabled on specified router devices now. It is turned off by default, choose which device should manage the suspension and turn it on in device edit page.
* Emails are now case insensitive - you can log in using name@examle.com or Name@EXAMPLE.com
* IP in CIDR format can no longer have netmask lower than 8
* Association between client service and network device is optional now. However, if you want to to use all current and future network features, it is recommended to link client service to a connect point network device)
* More user friendly log messages
* PHP updated to v7.0.11

### Fixed
* Stripe payment rounding error fixed
* Possible problems with system settings options now fixed (suspension feature could be still active although it had been switched off in system settings)
* CSV import bug fixed
* Position of button for Save invoice and Send invoice has been fixed
* Suspended service count fixed on homepage
* Fixed payment receipt email sending
* Suspend synchronization fixed after a new payment is added, client is correctly unsuspended in a few secs
* Email connection check fixed
* Problems when closing some modal windows and other minor UI fixes

## 2.0.14 (2016-09-07)

### Changed
* Various form validations added to avoid crashes
* Better confirmation dialog when demo mode is terminated

### Fixed
* Stripe payments passed to UCRM corretly now
* Invoice preview fixed and other UI fixes
* Minor fixes

## 2.0.13 (2016-08-30)
### Changed
* PHP updated to v. 7.0.10

### Fixed
* Crashes when creating invoices and approving drafts fixed
* Bug fixed when creating services after organization has been deleted

## 2.0.12 (2016-08-19)

### Added
* Payment receipts - You can send receipts manually or set up automatic receipts for incomming online payments (billing settings)
* Various form validations
* System logs enhancements

### Fixed
* Crashes while creating invoices fixed
* Minor fixes


## 2.0.11 (2016-08-16)

### Added
* Demo mode - enabling you to set real life data within a sandbox and test the app (clients will not be notified) Then launch the app to production mode
* Custom invoicing period start day (per client, per service)
* Help panel explaining invoicing parameters (click the tooltip icons on new service page)
* UCRM Time zone - you can set your local time zone in Settings > General > System

### Fixed
* Service status displayed correctly (suspended - red, terminated- grey)
* SSL redirect to custom port fixed (follow the knowledge base guide)
* Minor bug fixes


## 2.0.10 (2016-07-29)

### Fixed
 * Fixed client archive UI
 * Fixed cache permissions bug
 * Fixed service discount dates selection

## 2.0.9 (2016-07-28)

### Added
* Client init id number - new id is suggested automatically according to the last id used within the given organization
* You can now choose which rows to import in CSV import tool
* First and last name added to admin users
* MapBox satellite view
* Added AOA currency support

### Changed
* Device firewall/NAT rules are synchronized when UCRM ports are changed in system settings.
* Client can be moved to archive. Then the client can be deleted permanently.

### Fixed
* Skipped next invoicing day fixed
* Redirection to suspend page fixed
* Fixed file permission bug / crashes when unsuccessful write to the cache directory
* Fixed possible problem with PDF generator render
* Fixed validation message in new invoice form
* Date formating on invoice fixed and other minor bugs

## 2.0.8 (2016-07-15)

### Added
* Easy SSL support (Upload certificate files at Settings | Tools | SSL certificate and restart)
* Select boxes for clients now allow searching
* When creating an invoice you can also set up a new tax or product
* Invoiced revenue report PDF export
* Added PDF page size settings (US letter, US legal and A4)
* Additional form fields validations
* Added missing "approve" and "void" buttons for invoices in client's billing section

### Changed
* Admin users now can set their first and last name
* CSV import validation improved
* Better layout for user group permissions
* Invoice form now contains different buttons for "save" and "save and send" instead of checkbox to send email to client

### Fixed
* Fixed problems with deleted services, devices and sites
* Fixed suspend page error "File not found"
* Password reset fixed
* Attaching an invoice to new payment fixed
* Fixed background scripts execution
* Various minor fixes 

## 2.0.7 (2016-07-01)
 
### Added
 * Authorize.Net support for one-time payments
 * Client impersonation feature. As an admin user you can now log in to client zone and see exactly the same what the client can see.
 * Refunds feature. You can create a refund for client upto the amount of client's credit. (not connected to online payment gateways)
 * Custom CSV imports for entities: client, payment. You can upload your custom csv file and match the csv columns with corresponding entity attributes. (Settings | Tools | CSV import)
 * UCRM database backups are created periodically. Backup download and restore feature is enabled. (Settings | Tools | Database backup)
 * Invoices and Payments overview grid can be filtered and exported into pdf
 * Invoice notes for client (visible to client and placed into the invoice) and invoice notes for admin (not visible to client)
 * Personalization of email notifications is enabled using wysiwyg editor (Settings | General | Notifications)
 * You can setup/change port numbers used for UCRM app and UCRM suspend page.
 * Improvements in Tax settings (tax cannot be deleted because of reporting and accountant purposes, it can be replaced globally with new tax though)
 * Database encryption for mailer and device passwords. (Make sure to backup your encryption key, you can find it at /home/ucrm/data/ucrm/data/encryption/crypto.key)
 * Organization based invoice template settings - You can set whether to include tax id and bank account into invoice)
 * User actions are logged now. Actions such as generating invoices, batch actions, logins, etc.
 * You can add manually a custom log entry to each client.

### Changed 
 * Service IP is not validated against router IP ranges (changed to recommendation)
 * Client id is validated to be unique now.
 * Vast performance improvements
 * More user friendly Device interface form
 * Payment entity always comprises currency now
 * Client search should now provide better results
 * Better grid pagination (items per page, control links)
 * Service name now not required and inherited from service plan if not provided
 * Mailer now uses "Sender address" from settings as "Sender" email header and includes "From" field as well
 * Editing "Invoicing from" field on service now possible, if no invoice exists for the service
 * "U CRM Billing" renamed to "UCRM"
 * "Tariffs" renamed to "Service plans"
 * Minor UI changes
 
### Fixed 
 * Sending notifications for overdue invoices is handled properly
 * Service status is reloaded after every change (when suspended or stopped)
 * Fixed password reset for clients and admins
 * Fixed GPS address resolving
 * Fixed duplicate client ID error in new client form
 * Using new user groups with custom permissions works properly now.
 

## 2.0.6 (2016-05-31)
 
### Added
 * Recurring payments - client can set up an automated billing plan based on recurring invoice
 * New billing reports: Taxed amount and Invoiced revenue
 * Search clients using single input for name, phone, email, street or city. This search can even handle typing errors. Additionally, you can search for client by id using this prefix "id:", e.g id:142 will search for client with id 142
 * Late fee can be chosen to be fixed amount or percentage.
 * Fully qualified domain name of the UCRM app has been added to system settings. If provided, it will be used in redirects and email notifications sent to clients
 * Invoice batch printing into pdf using grid filters
 * System log - all user actions are logged now
 * Anonymous statistics
 * 500 Internal Server Error page now contains encoded error message (small grey text at the bottom of page). Please provide the UBNT team with a copy of this text when an error occurs

### Changed 
 * Device information and IPs removed from client zone
 * Now you can add service IP in 3 formats - single IP, range from-to and CIDR format

### Fixed 
 * Suspension postpone redirects to proper port number
 * Overdue invoice notifications are sent correctly
 * Minor UI fixes

## 2.0.5 (2016-05-13)
* Fixed possible file upload problem
* Fixed organization logo and stamp in invoice PDF
* Fixed image thumbnail cache
* Small UI fixes

## 2.0.4 (2016-05-12)
* Fixed PDF generator

## 2.0.3 (2016-05-12)
* Fixed zip package importing in the Setup wizard
* Additional app speed enhancements

## 2.0.2 (2016-05-11)
 
### Added
 * Major app speed enhancement
 * Uninstall script

### Changed 
 * Paid or partially paid invoice can not be edited now, it can be deleted though
 * Installation script improved (does not change postgre password when run more than once) 

### Fixed 
 * Draft bulk approving of recurring invoices fixed
 * Change password feature fixed
 

## 2.0.1 (2016-05-05)

### Fixed
* Sending emails and notifications fixed
* Password fields are no longer visible
* Invoice style sheets fixed
* Tooltips position and other minor UI fixes

### Added
* New feature to test mailer connection and send test email
* Mailer log. All notifications and emails to clients are logged now
* Version of current U CRM Billing displayed on the homepage

### Changed
* Setup of the mailer settings simplified
* Logging into the setup wizard is no longer needed

## 2.0.0 (2016-04-29)

### Manage entities

* Organizations
* Clients
* Tariffs (What internet plan are offered by the organization)
* Client's services (Ordered tariff by a client. Ability to override price, invoicing period etc.)
* Products (other products or one time services offered by the organization)
* Network entities: Sites, Devices, Interfaces
* Admin users, roles, permissions
* Settings (e.g. taxes, currencies, surcharges, default invoicing parameters etc.)

### Billing
* Manual invoicing
* Recurring invoicing at user defined day and time
* Automatic late fees
* Proration of first & last month billed
* Notifications
* Invoice handling
* Batch invoicing
* Invoice printable export into pdf
* Invoice preview (for both manual and recurring invoices)
* Edit/void invoice until paid

### Payments
* Manual payment input
* Gateways integration: PayPal, Stripe
* Payments matching
* Overpayments turning into credit
* Payment in advance - whole payment turns into credit

### Billing & control
* Suspend & late fee & walled garden
* Onetime postpone the suspension by client in order to be able to pay
* Postpone the suspension by admin

### App features
* Setup wizard
* Basic data migration from AirCrm Beta

### Client's site
* Overview of invoices, payments, account balance, contact form, change password
* Payment gateway



