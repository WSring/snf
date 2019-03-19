# snf
Fediverse parts for Friendica only

For all those like me, having the need to support admin triggered email invitations 
in a multilingual environment, I just changed some code. The solved problem was, an 
instance has a default LC (language code), the instance admin may has assigned a 
(perhaps different) LC for self, and now wants to invite a new user who even needs 
a quit different LC else.

Example: when an instance is driven with default LC of "de" because it's located in 
Germany, while the admin prefers "en" for the own account and the dashboard, and now 
has to invite a spanish individual.

Files:
******
mod/admin.php
view/lang/de/admin_invite_email.md
view/lang/en-gb/admin_invite_email.md
view/lang/en-us/admin_invite_email.md
view/lang/es/admin_invite_email.md
view/template/admin/users.tpl

Modified functions:
*******************
admin_page_users_post()

