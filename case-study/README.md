# Approach
There are two types of users that this application needs to cater to: people registering their first dog(s) and people returning to renew a license or register a new dog. While the former would be totally new to the application, the latter will still not be exposed to it frequently enough to develop a sense of familiarity. Therefore, adopting a beginner's mindset is going to be very important when looking for areas for improvement. If I was too familiar with the system in question, I would look for someone else who was not as familiar and guide them through a common use case while observing their reactions.

In this particular case, I've never owned a dog and therefore did not have any familiarity with the application. I found that even though I did not have any confusion when trying to fill out the application as far as information requested, I was left quite frustrated by the implementation of the form itself. The appendix includes a comprehensive list of areas for improvement.

After gaining user feedback, I would gather requirements from key stakeholders, in this case likely the department that issues dog licenses. I would first look for any documents written upon completion of the existing application, summarize my findings, and go to said stakeholders to clarify and update these needs.

I would then work with designers to make the established improvements, additionally addressing any new requirements that arose during the check in with stakeholders. Throughout this design process, I would loop in developers to ensure technical feasibility.

Upon completion of the design, it is up to developers to create a working front end for the application. Once that has been implemented, I would make sure to review using the same beginner's mindset approach to ensure the new experience is seemless, and perhaps even delightful. If all tests pass, the front end can be fully integrated with the overarching system, leading to project completion.

# Challenges
Most challenges are likely going to be based on communication. While the main goal is to improve the user experience, we still have to balance our efforts with keeping the data-gathering requirements in check. Checking in often enough with the department that issues licenses to ensure they are on the same page while keeping in mind that they are potentially nontechnical will go a long way to ensuring the end-product meets everyone's needs.

Similarly, development is a resource that needs to be balanced against all of the potential improvements that can be made. Keeping engineering in the loop so that each improvement's cost is evaluated will ensure that the most impactful improvements are prioritized.

Lastly, it is always important to recognize that it can be difficult for teams to fully anticipate user's needs. Getting continuous feedback during key stages of development to verify progress would be of utmost importance to ensuring successful completion of the project.

# Appendix
## Assumptions
* Each licensed dog has its own license number
* Uploading rabies certificate copies is required

## Areas for improvement by form page
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
  * Phone Number and Alternative Phone Number fields are labeled Home and Cell on the Review page - this is an inconsistency
  * (opportunity for delight) Fields could be edited inline, by rendering the corresponding form while in edit mode