# Changelog

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



