# Prompt
In the City of Boston, if you have a dog that's older than six months you must get them licensed. The [online application](https://www.boston.gov/departments/animal-care-and-control/how-license-your-dog/) is on our product roadmap for improvement. How would you think about enhancing this online experience? What would your process look like? What challenges do you foresee? How would you address them? Our expectation is that this is not an extensive plan, we're more interested to hear in brief your approach to the project.




# How to think about enhancing the experience

# What would the process of enhancing look like?

# Foreseen challenges

# How to address challenges

# Appendix
## Assumptions
* Each licensed dog has its own license number
* Rabies certificates are required

## Areas for improvement by page
* ### Global
  * Form state could be stored locally in case user accidentally navigates away or wants to finish submission later
  * Navigation between form pages could be improved by enabling navigation directly to desired page rather than only by using prev/next buttons
  * Currently no indicator for optional fields
  * Certain fields should only render when prerequisite conditions are met (e.g. spay/neuter certificate should only render if dog is spayed/neutered)
  * Typography - text should be made more readable by generally increasing font size
  * There is no field validation or feedback until the user gets to the Review page
  * The site is not responsive, creating a poor mobile experience

* ### Owner Info
  * Phone number - could automatically format to improve readibility, rather than being a string solely containing numbers. The label should also not have the format, as this would likely hinder accessibility.
  * Email - No validation for valid format, even on the Review page.
  * Street address - No validation for valid address - could use an address API to render options as the user types. Could also be broken up into further subfields.

* ### Dog Info
  * Application type should be a hidden field whose value is inferred based on earlier field entries
  * There should be a page/view asking how many dogs are being registered - only 3 are currently possible, and toggling the 'Application Type' to essentially add more dogs is quite clunky
  * Age should have clearer labels - it's not clear how the Year and Month fields should be formatted, if both are required, etc
  * Color - The options could be consolidated, compensated by adding an "Other" field. This would be less overwhelming than having a long list of options
  * Breed - many dog owners do not know their dog's breed, yet there is no discoverable corresponding option
  * Since a lot of this information is to be utilized if the dog goes missing, it should be possible to optionally upload a photo
  * Spayed/Neutered should be a checkbox rather than a sex selection

* ### Review
  * Missing rabies certificates does not lead to a validation error
  * "Click here to edit" is not accessible hyperlink text
  * Phone Number and Alternative Phone Number fields are labeled Home and Cell on the Review page - this is inconsistency
  * (opportunity for delight) Fields could be edited inline, by rendering the corresponding form while in edit mode