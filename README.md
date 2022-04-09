# Email Preparator

The __Email Preparator__ is a tool for event organisers who may need to reach and coordinate dozens of presenters, sponsors, workshop participants, etc.

It's a Google Sheet that interacts with your Gmail and Drive accounts to build emails with attachments. You can make a copy for your own use for free.

* [Email Preparator v0.1](https://docs.google.com/spreadsheets/d/18v8caw4R5WscY6k8qZ73LuBmX0iTQ-jouKjcf9YRnVw/copy)
* [Email Preparator v0.2](https://docs.google.com/spreadsheets/d/1dRD1mYxWgdFJl4dIBJMKFa339auvbErk6XtT8qjlq0o/copy)

The Email Preparator is provided free, and as-is, for use. It's a tool I use, and I'll occasionally update it. When I do, I'll create a new version so that you can continue to use the old sheet or transfer to the new one as you decide.

Cheers!<br>Lewis

## Welcome

The Preparator will create emails from templates you provide, to recipients you specify. All you need to know is a little HTML to get started.

Drafts created by the Preparator will appear in your Gmail drafts folder - where you can review and action them.

_NB. Scripts on Google Drive are time limited, and this creates a natural barrier to abuse. You cannot and should not use the Preparator to send emails to people without their consent, and you will not be able to send bulk volumes of email using this tool._

### Changelog

| Version  | Changes |
| ------------- | ------------- |
| 0.1 | Initial release with support for Recipients, Templates, Variables, Attachments, Drafting Logging |
| 0.2 | Assorted minor improvements |

### Issues and feedback

Please record feedback using [Issues](https://github.com/instantiator/Email-Preparator/issues) for this repository.

## Getting started

* Make a copy of the preparator using the link above.
* Edit the white cells. Data in the shaded cells will be filled in by the Preparator.
* To compose emails, use the __Draft emails...__ action from the sheet's __Email Generator__ menu.
* Once ready, new emails will appear in your Gmail drafts folder.

### Adding Recipients

You can add recipients in the __Recipients__ view. Specify their email address, and the templates they should receive.

If you leave the email address blank, the __Preparator__ will still create drafts for you, but they won't have anybody in the __To:__ field.

Templates are detailed in the __Template__ view, and may refer to variables defined in the __Variables__ view or the __Recipients__ view.

Add extra variables to the __Recipients__ view by adding columns there and wrapping variable names in double curly braces, eg. `{{name}}` - this then allows you to use `{{name}}` in a template and have real values substituted when drafting emails.

### Making Templates

Create templates in the Templates view by giving them a _Template ID_ (referred to in the _Recipients_ view), and then providing a _subject_, a _body_, and the _Attachment IDs_ for any attachments the emails should have.

Template bodies are written in simple HTML. It's not a good idea to include HTML in subject lines.

In either the subject or the body, you may refer to variables (defined in the Variables view or the Recipients view) by wrapping the variable name in curly braces, eg. `{{name}}`

When an email is drafted, the variable names will be replaced by their values - so you can create custom emails for each of your recipients and templates.

### Variables

Templates in the __Templates__ view define body and subject for emails, and each can contain variables defined either in the __Variables__ view, or in the __Recipients__ view (as extra columns).

Refer to variables in the body and subject by wrapping them in curly braces, eg. `{{name}}`

Add variables to the __Variables__ view by defining their name, and their value.

Add variables to the __Recipients__ view by adding extra columns, with the variable name wrapped in curly braces. You can then define the values for these variables per recipient in the rows below.

### Images

Inline images have not yet been implemented.

### Attachments

List all attachments you wish to refer to in your templates, by giving them an _Attachment ID_, and providing their _Drive ID_ in the _Attachments_ sheet.

You can provide comma-separated lists of _Attachment IDs_ in the _Templates_ view to add attachments to any template.

#### Drive IDs

To find the __Drive ID__ of a file in Google Drive, open the file in a new window in drive so that the URL points directly to the file.

_(eg. for images, double click the image to preview it, and then choose Open in new window from the menu in the top right.)_

Look at the URL of the new tab. It contains the __Drive ID__.

eg.

* In this URL: https://drive.google.com/file/d/1TIshDLPzSAJSiHqFR_qdHBXYK7FvHpRx/view
* The Drive ID of the file is: `1TIshDLPzSAJSiHqFR_qdHBXYK7FvHpRx`

### Log

The log contains details of each attempted draft, if it succeeded or if it failed (and why).

If nothing seems to have happened when you draft a set of emails, check your Log to see why.
