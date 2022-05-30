Validational Rules 
Validation rules are conditions that should be met before an object is stored in the database. They are placed on the attributes in the Domain Model. When you add a validation rule, you can also enter a custom error message that will be shown when the validation rule is not matched.

Adding validation to the Domain Model means that every component, page, or microflow in your project using that object must pass the validation check. If you apply validation here, it’s applied everywhere

Adding validation to microflows makes the validation rules more accessible and visible for everyone. Those rules are also easily updated without impacting the underlying domain model.

Adding validation to pages only applies on that page, not in other places. Also you can only have one validation rule per field. A course title can’t be both required and unique if you use a page validation.

So, what happens if the object doesn't pass the validation check? Well, depending on where in the app the validation was triggered there are three possible results:

Page, with an input widget for the attribute: The end-user tried to add an object to the database, using a page that has an input widget for the attribute, but did not fill it out correctly. In that case an error message appears underneath the input widget.

Page, without an input widget for the attribute: The end-user tried to add an object to the database, but the attribute that didn't pass the check doesn't have an input widget on the page the end-user is currently looking at. A pop-up message appears, with the error message in it.

Microflow: A microflow attempts to commit the object to the database. In that case an error message appears in the log.


 A Regular Expression is a sequence of characters that defines a search pattern. Good examples are bank account numbers or email addresses. Let’s look at email addresses a little more. An email address has a pattern: something@something.sth. So some characters first, then an @ sign, then some more characters, a dot (.) and then the extension. A Regular Expression can check whether the email address that has been filled out matches this pattern or not. Anything which does not conform to the pattern, for example something$sth, wouldn't pass as a valid email address
 You don't have to know how to write Regular Expressions, because this can be quite challenging. Just use your favorite search engine and look for Regex and then the thing you want to validate. Regex is the abbreviation for Regular Expression. For example: Regex Email.
 
 The first section, multiplicity, shows you what type an association is.

The next two options show you the delete behavior settings. In other words, what should happen when you delete one of the associated objects. In the example, when you want to delete the ‘TrainingEvent’ object, you have three options:

Keep ‘Registration’ object(s). This means that you will be able to delete the training event and all the registrations that belong to it will stay in the system. This is also called no predefinition and is the default setting for delete behavior.

Delete ‘Registration’ object(s) as well. This means the training event and all registrations that belong to it will be deleted from the system.

Delete ‘TrainingEvent’ object only if it is not associated with ‘Registration’ object(s). This means that the training event can only be deleted if it doesn’t have any registrations connected to it yet. This type of delete behavior is called prevention of delete. When selecting this, you also get the option to show an error message to the end-user, informing them why they cannot delete a certain object.

