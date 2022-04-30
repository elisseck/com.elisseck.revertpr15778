# com.elisseck.revertpr15778

See https://github.com/civicrm/civicrm-core/pull/15778 and https://lab.civicrm.org/dev/core/-/issues/1378

This extension will override CRM/Core/BAO/ActionSchedule.php L607 setting $polite to FALSE to turn off the new CRM/Contact/BAO/Contact.php L2570 query

`if ($polite) {
     $query .= '
     AND civicrm_contact.do_not_email = 0
     AND civicrm_email.on_hold = 0';
   }`

This modification will "turn off" the feature until an admin feature to override is put in place. Described in https://lab.civicrm.org/dev/core/-/issues/1513 but not implemented.
