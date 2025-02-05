# My Finances Tracker App

(Developer: Gabriela Fabiola Paredes Rojas)

![Mockup image](documentation/website-screenshots/1-mockup.png)

**Welcome to MyFinances tracker APP!**

  This expense tracker will help you monitor
  your income and expenses!
  Are you ready to understand your spending habits?
  Let's go!

+ The live page can be accessed via this [link]()

---
## Project Goals

### User Goals

+ Track and manage income and expenses on a monthly basis.
+ Generate monthly financial reports displaying total income, total expenses and cash balance (total income - total expenses).
+ Check spending patterns by viewing categorized expenses and identifying the highest expense category.
+ Quickly and easily add new income and expense entries.
+ View all their income and expense data.

### Site Owner Goals

+ Create a practical and user-friendly application to help users effectively monitor their income and expenses.
+ Ensure application functionality and bug-free performance.
+ Create an intuitive user interface.
+ Create an easy to use app.
  
---
## User Experience

### Target audience

+ Individuals who want to have an overview of their income and expenses.
+ Users who want to understand their spending habits.
+ Any user who is comfortable with using a simple computer program.
+ Users searching for a free and easy way to track finances.


### User expectations

+ Clearly understand the application's purpose.
+ Quickly and easily access the menu content.
+ Correctly store and display income and expense entries.
+ Their income and/or expense entries must be stored and displayed correctly. 
+ The monthly finance report must correctly calculate and display total income, total expenses, cash balance, expenses per category, and the highest expense.
+ The application must warn the user of any invalid input.

### User stories

+ **As a first-time user, I want to:**

  + Quickly understand the purpose of the application.
  + Have clarity in the menu options so I can find easily desired functions.
  + Have clear and easy to follow application instructions.
  + Have my results displayed clearly and concisely, using appropriate formatting and labels for easy interpretation.
  + Have a enjoyable experience without delays or glitches or errors.
  + Have an application that is visually appealing to enhance the user experience.

+ **As a returning user, I want to:**

  + Be able to quickly complete common tasks (e.g., adding income, adding expenses, generating a report), leveraging the past experience with the program.
  + The application's interface and core functionality to remain unchanged from the previous version I used, except for explicitly documented updates.
  + Have my financial data available to me within seconds, if I select to have it displayed.
  + Accomplish their tasks quickly and easily, 
  + Expect their data to be readily accessible.
  + Have an application that continues to provide value and help them monitor their finances effectively.
  + Continue having the same core financial tracking features (e.g., income/expense tracking, reporting), allowing me to monitor my finances with the same level of detail as before.

+ **As the site ownser, I want:**

  + Regularly update the website with new menu options and features (e.g., monthly, quarterly, yearly reports) to maintain user engagement.
  + Ensure a smooth and accessible user experience by regularly testing the website on different devices and browsers and addressing any reported accessibility issues within.
  + To keep the application running correctly, be free of bugs, and not crash.
  + Collect user feedback to understand user needs and identify areas for improvement.

---
## Features 

### Welcome message

![Welcome message](documentation/website-screenshots/2-welcome-message.png)
  
+ Positioned above the menu options.
+ The welcome() function displays a colorful welcome message to the user when the program starts. It uses the colorama library to add green borders, creating a visually appealing introduction to MyFinances app.
+ The welcome message already informs the user that what can be done in the program and that it is easy to use.
       
### Menu options

![Menu options](documentation/website-screenshots/3-menu-options.png)

The Menu provides the following options:

*   **0: Application Instructions:** Learn how to use MyFinances.
*   **1: Add New Income:** Record a new income entry, by specifying the month, source, and amount.
*   **2: Add New Expense:** Record a new expense entry, by specifying the month, category, description, and amount.
*   **3: View All Records:** Display all income and expense entries in a table format.
*   **4: Monthly Finance Report:** Generate a detailed report for a specific month, showing total income, total expenses, cash balance, and a breakdown of expenses by category.
*   **E: Exit:** Close the application.

+ It gets the user selection and validates the selection.

+ Including spaces to the inputs is accepted. 

+ If an invalid input is entered (e.g., non-numeric characters or a number outside the valid range: 0-4), an error message is displayed, and the user is prompted to select a menu option (0-4 or E) again. 

+ All invalid inputs are handled with a clear error message. (Figures below).

![Empty input](documentation/website-screenshots/4-empty-invalid-input.png)

![Invalid choice](documentation/website-screenshots/5-invalid-choice-not-number-from-0-to-4-or-E.png)

![Invalid choice](documentation/website-screenshots/6-invalid-choice-not-number-from-0-to-4-or-E.png)

+ E or e are accepted as valid inputs to exit the application and a GoodBye message is displayed (Figures below).

![Valid choice "e"](documentation/website-screenshots/7-lowercase-valid-input-exit.png)

![Valid choice "E"](documentation/website-screenshots/8-uppercase-valid-input-exit.png)

**Menu Option 0**

+ **User inputs 0:**

![Menu option 0](documentation/website-screenshots/9-user-selection-option0.png)

+ **Application Instructions:** The application provides comprehensive instructions accessible from the main menu. These instructions cover each available feature in detail:
    *   **Adding Income:**  Users can record new income entries, specifying the month, source, and amount. The instructions explain the required format for each field and highlight the use of the European currency format for amounts.
    *   **Adding Expenses:** Users can record expenses, providing the month, category, description, and amount. Similar to income entries, the instructions detail the expected input format and the use of the European currency format.
    *   **Generating Monthly Reports:** Users can generate detailed financial reports for any month of 2025. These reports include total income, total expenses, cash balance, a breakdown of expenses by category, and the highest expense category.
    *   **Viewing All Records:** Users can view all their stored income and expense records in a tabular format. This allows for easy review and analysis of their financial data.
    *   **Exiting the Program:** Users can exit the application when finished.  The instructions reassure users that their data is safely stored.

+ **Return to Menu / Exit Prompt:** After the applications instructions are displayed, the application prompts the user to either return to the main menu or exit the program. This provides a controlled flow within the application.  Invalid input (anything other than 'M' or 'E', or "m" or "e") is handled with a clear error message.

![Empty input](documentation/website-screenshots/4-empty-invalid-input.png)

![Invalid choice](documentation/website-screenshots/5-invalid-choice-not-number-from-0-to-4-or-E.png)

![Invalid choice](documentation/website-screenshots/6-invalid-choice-not-number-from-0-to-4-or-E.png)

![Invalid input example](documentation/website-screenshots/14-from-option0-invalid-input-example.png)

**Menu Option 1**

+ **User inputs 1:**

![Menu option 1](documentation/website-screenshots/15-user-selection-option1.png)

*   **Adding Income:** Users can easily record their income for 2025. The application guides them through the process, prompting for:
    *   **Month:** The month the income was earned (e.g., January). The application accepts full month names.
    *   **Source:** The source of the income (e.g., Salary, Freelance).  The application validates that the source is at least 4 characters long and isn't entirely numeric.
    *   **Amount:** The amount earned. The application displays and stores the amount using the standard European currency format (e.g., 1.500,00 EUR).  
    
+ All input fields are required and cannot be left empty.

+ Leading/trailing spaces are accepted (e.g., JanuarY, January, january, "    January", etc. are all accepted).

+ Including capitalization to month and source inputs is accepted.

+ The amount must be a positive number (no negative signs) and contain only digits (no special characters or letters).

+ All invalid inputs are handled with a clear error message. Examples below:

![Invalid empty input](documentation/website-screenshots/19-empty-invalid-input.png)

![Invalid month](documentation/website-screenshots/20-invalid-month-name.png)

![Invalid source](documentation/website-screenshots/21-invalid-source-input.png)

![Invalid amount](documentation/website-screenshots/22-invalid-amount-input.png)

+ After entering the details, the application displays a message of the added income (month, source, and amount) confirming that the new income entry has been successfully stored. 

+ Users are then given the option to add another income entry, add an expense entry, return to the main menu, or exit the application. 

![New income data displayed, and the user is prompted for further action](documentation/website-screenshots/16-income-data-added.png)

+ The application validates user input for these options as well, displaying an error message for invalid choices (figure below).

![Invalid option example](documentation/website-screenshots/17-invalid-input-example.png)

+ The new income record is appended (stored) to the my_finances Google cloud "incomes" worksheet (figure below).

![my_finances incomes worksheet](documentation/website-screenshots/18-income-addded-to-google-income-worksheet.png)

**Menu Option 2**

+ **User inputs 2:**

![Menu option 2](documentation/website-screenshots)

+   **Adding Expenses:** Users can easily record their expenses for 2025. The application prompts for the following information:
    -   **Month:** The month the expense was incurred (e.g., January).  Full month names are accepted.
    -   **Category:** The category of the expense (e.g., Rent, Groceries).  Input must be at least 4 characters long and cannot be entirely numeric.
    -   **Description:** A description of the expense (e.g., Monthly rent, Weekly groceries). Input must be at least 4 characters long and cannot be entirely numeric.
    -   **Amount:** The amount spent. The application displays and stores the amount using the standard European currency format (e.g., 1.500,00 EUR). 
  
+ All input fields are required and cannot be left empty.

+ Leading/trailing spaces are accepted (e.g., JanuarY, January, january, "    January", etc. are all accepted).

+ Including capitalization to month, category and description inputs is accepted.

+ The amount must be a positive number (no negative signs) and contain only digits (no special characters (except from the sign +) or letters).

+ All invalid inputs are handled with a clear error message. Examples below:

![Invalid empty input](documentation/website-screenshots/23-empty-invalid-input.png)

![Invalid month](documentation/website-screenshots/24-invalid-month-input.png)

![Invalid category](documentation/website-screenshots/25-invalid-category-input.png)

![Invalid description](documentation/website-screenshots/26-invalid-description-input.png)

![Invalid amount](documentation/website-screenshots/27-invalid-amount-input.png)

+ After entering the details, the application displays a message of the added expense (month, category, description and amount) confirming that the new expense entry has been successfully stored. 

+ Users are then given the option to add another expense entry, add an income entry, return to the main menu, or exit the application. 

![New expense data displayed, and the user is prompted for further action](documentation/website-screenshots/28-expense-data-added.png)

+ The application validates user input for these options as well, displaying an error message for invalid choices (figure below).

![Invalid option example](documentation/website-screenshots/29-invalid-input-example.png)

+ The new expense record is appended (stored) to the my_finances Google cloud "expenses" worksheet (figure below).

![my_finances expenses worksheet](documentation/website-screenshots/30-expense-added-to-google-income-worksheet.png)

**Menu Option 3**

+ **User inputs 3:**

![Menu option 3](documentation/website-screenshots/31-user-selection-option3.png)

*   **Viewing Income and Expense Data:** Users can view all recorded income or expense data in a tabular format. 

+ The application retrieves the data from the specified worksheet (Incomes or Expenses) and displays it in a well-formatted table.

+ The table includes headers for each column, making the data easy to understand.

![display all income and expense data](documentation/website-screenshots/32-display-all-incomes-and-expenses.png)

+ If a worksheet contains no data, the application displays a message indicating that no data is available.
MISSING

+ The program then asks the user what they would like to do next, and displays the menu options again, with the same validations as in, for example, menu option 0. 

**Menu Option 4**

+ **User inputs 4:**

![Menu option 4](documentation/website-screenshots/33-user-selection-option4.png)

+   **Generating Monthly Finance Reports:** Users can generate detailed financial reports for any month of 2025. The report includes:
    -   **Total Income:**  The sum of all income entries for the selected month, displayed in European currency format.
    -   **Total Expenses:** The sum of all expense entries for the selected month, displayed in European currency format.
    -   **Cash Balance:** The difference between total income and total expenses for the selected month, displayed in European currency format. 
    The application clearly indicates whether the balance is positive or negative.
    -   **Expense Breakdown by Category:** A detailed breakdown of expenses for the selected month, showing the total amount spent in each category, displayed in European currency format.
    -   **Highest Expense Category:** The expense category with the highest total spending for the selected month, also displayed in European currency format.

+ The application first displays the report title in green using colorama to stand out and then prompts the user to enter the month for the report (figure above).

+ Month input field is required and cannot be left empty.

![Invalid empty input](documentation/website-screenshots/34-empty-invalid-input.png)

+ The application validates the user input for the month, ensuring it is a valid month name. Full month names are accepted.

+ Leading/trailing spaces are accepted (e.g., JanuarY, January, january, "    January", etc).

+ If the user enters an invalid month name (e.g., jan, or a misspelled month) and an error message is displayed.
![Invalid month](documentation/website-screenshots/35-invalid-month-input.png)

+ If there is neither income nor expense data for the selected month, a message will be displayed indicating there is no data for that month yet.

![Month has no data](documentation/website-screenshots/35-month-has-no-data.png)

+ For a valid month input where there is income data but no expenses data, a warning message will be displayed indicating there is no expense data. In this case, the report displays total income, total expenses (0,00 EUR), cash balance, and in "expenses by category" another warning message that no expenses for this month exists.

![No expense data](documentation/website-screenshots/36-no-expense-data-for-that-month.png)

+ For a valid month input where there is expense data but no income data, a warning message will be displayed indicating there is no income data. In this case, the report displays total income (0,00 EUR), total expenses, cash balance, expenses by category, and highest expense.

![No income data](documentation/website-screenshots/37-no-income-data-for-that-month.png)

+ For a valid month input, where both, income and expenses data exist, the report displays total income, total expenses, cash balance, expenses by category, and the highest expense.

![monthly report](documentation/website-screenshots/38-total-income-and-expenses-calculation.pngg)

The program then asks the user what they would like to do next, and displays the menu options again, with the same validations as in, for example, menu option 0. 

**Menu Option E**

![Menu option E](documentation/website-screenshots/7-lowercase-valid-input-exit.png)

+ **Exiting the Program:** The application provides a clean exit, displaying a friendly farewell message to the user before closing.
+ This ensures a positive user experience even when leaving the application.
+ Both "e" or E" are recognized as a valid input to exit the program (figures above and below, respectively).

![Menu option E](documentation/website-screenshots/8-uppercase-valid-input-exit.png)

---
## Features left to implement

+ This project allowed me to apply my understanding of Python, object-oriented programming principles, and core programming concepts like flow control, iteration, conditional statements, functions, methods, and data structures. While I acknowdlege that a complete finance application would include more features (which I intend to add later), my focus here was on these fundamentals. 

+ Among features left to implement:

  +   **Data Editing and Deletion:** Allow users to correct mistakes, or delete their entries, to manage their financial data more effectively.

  +   **Searching:** As the data grows, it will become more difficult to find specific entries. Implementing searching capabilities would allow users to quickly locate the income or expense records they need.

  +   **Data Visualization:** While the monthly report provides a summary, visual representations of the data (charts, graphs) would make it easier for users to understand their spending habits and identify trends.

  +   **Multiple Years:** The application is currently designed to track finances for 2025 only. Future versions could allow users to select the year for tracking.

  +   **Error Handling/Input Validation Improvements:** While basic input validation is implemented, semantic validation of the "source," "category," and "description" fields could be added to further ensure meaningful input. However, to maintain flexibility for users, I have intentionally not implemented strict semantic validation at this stage, as the potential entries for these fields are limitless.  

---
## Design

### Color scheme

**Main color scheme**

![Main Color scheme](documentation/design/main-color-scheme.png)

- The russian violet (blue), seasalt (white) and davy's gray color where used as the main colors of the website. Their choice was inspired by the universe background image and their used keeps the website cohesive.

- The russian violet (blue) was used for the titles, button names and the paragraph within the Game indications section.

- All buttons except for the button with class btn--restart, used as box shadow the color davy's gray color. 

**Secondary color scheme**

![Secondary Color scheme](documentation/design/secondary-color-scheme.png)

- To simulate colors of the universe the hover effect used two colors as gradient: Royal purple ( #7943af) and Sapphire ( #3455af). 

- The button with the class btn--restart and the congratulatory message are styled in Sinopia orange to ensure that they stand out. This vibrant choice draws attention to the restart option, making it easy for users to replay the game, and highlights the victory message effectively, celebrating the user's success in a visually striking way.

### Typography

- "Rajdhani" and "Roboto" from Google Fonts were used as the primary and secondary font of the website, respectively. 
- The generic family name is "Sans-serif".
- For the titles (h1 and h2) letter-spacing CSS property with a value of 0.3rem was used, to add a slight space between letters in the text.

![Primary Font](documentation/design/primary-font.png)
![Secondary Font](documentation/design/secondary-font.png)

---
## Wireframes

#### Mobile

- [Mobile: Home menu page](documentation/wireframes/main-page-mobile.png)
- [Mobile: Games indications page](documentation/wireframes/game-instructions-mobile.png)
- [Mobile: Memory board game page](documentation/wireframes/memory-board-game-mobile.png)
- [Mobile: Congratulations page](documentation/wireframes/congratulations-mobile.png)

---
## Technologies used
- [HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Gitpod](https://www.gitpod.io/): the development environment to create the project files, folders and html, css and javascript codes.
- [GitHub](https://github.com/): to store the repository, bug track and see the deployed version.
- [Balsamiq](https://balsamiq.com/): to create the wireframes.
- [Google Fonts](https://fonts.google.com/): to import the Rajdhani and Roboto family fonts.
- [TinyPNG](https://tinypng.com/): to compress the images.
- [Flaticon](https://www.flaticon.com/): source of the memory card images.
- [Favicon.io](https://favicon.io/): source of the favicon images.
- [Am I responsive?](https://ui.dev/amiresponsive): to generate the responsive mockup image.
- [MDN Web Docs](https://developer.mozilla.org/en-US/): resource to check CSS properties and javascript syntax and definition descriptions.
- [Color-hex](https://www.color-hex.com/): to get the rgb color information.
- [Chrome DevTools](https://developer.chrome.com/docs/devtools?hl=de) and its open source [Lighthouse](https://developer.chrome.com/docs/lighthouse?hl=de).
-  [W3C HTML](https://validator.w3.org/) and [W3C CSS](https://jigsaw.w3.org/css-validator/) Validation Services. 
- [JSHint](https://jshint.com/): to detect errors and potential problems in the JavaScript code.
- [WAVE](https://wave.webaim.org/): to test accessibility.
- [DeepL Write](https://www.deepl.com/en/write): to spot spelling mistakes in the text. 

---
## Testing

### Validation
- In this section, the HTML and CSS codes were checked for compliance with industry standards. This was done using the W3C Markup Validation Service for HTML and CSS respectively, using the code from both: the working environment and the the deployed version.

- The result in both reports: no errors were returned.

#### HTML Validation

![HTML Validation](documentation/validation/html-file-validator.png)


+ There were no errors found in the javascript code using the JS Hint Validator. 

### Accessibility 

Accessibility was tested using the Web Accessibility Evaluation Tool (WAVE report below), and no errors were reported. 

![WAVE report](documentation/wave/wave-report.png)

### LightHouse report

Lighthouse tool from Devtools was used to confirm that the website is performing well, is accessible and the colors and fonts chosen are readable.

![LightHouse report Home menu page](documentation/lighthouse/lighthouse-report-homepage.png.png)

### Responsiveness

- The website was checked across devices using the chrome extension [Responsive Viewer](https://chromewebstore.google.com/detail/responsive-viewer/inmopeiepgfljkpkidclfgbgbmfcennb?hl=en). 

- In addition, it was manually checked in the following devices:
  - Huawei Y9 Prime 2019
  - Iphone XR
  - Iphone 15 pro
  - Samsung Galaxy S8

### Manual Testing

| Feature | Action | Expected result | Tested | Passed | Observations |
| --- | --- | --- | --- | --- | --- |
| **Home Menu Page** | | | | | |
| Header | Game name display | The title is centered and positioned as the topmost element on the page and it is readable | Yes | Yes | - |- |
| Play Game! button | Click on the Play Game! button | Redirects to the Memory Board Game page | Yes | Yes | - |
| Play Instructions button | Click on the Play Instructions button | Redirects to the Game Indications page | Yes | Yes | - |
| Both Home menu buttons | Hover over them | The buttons will rotate slightly and change colors to a gradient of blue and purple | Yes | Yes | 
| Both Home menu buttons | Buttons displayed | The buttons are centered one of top of the other with a consisting style, and they are readable | Yes | Yes | 
| **Game Indications Page** | | | | | |
| Header | Game name display | The title is centered and positioned as the topmost element on the page and it is readable | Yes | Yes | - |- |
| Game indications text | Text display| The paragraph stands out, the content is justified with no spelling mistakes | Yes | Yes | - |
| Images | Images display | The images are loading correctly, they have the same style and dimensions, and are located  below the text| Yes | Yes | - |
| Home Menu button | Click on the Home Menu button | Redirects to the Home Menu page | Yes | Yes | - |
| **Memory Board Game Page** | | | | | |
| Header | Game name display | The title is centered and positioned as the topmost element on the page and it is readable | Yes | Yes | - |- |
| Game Board | Game board display | It stands out and it is centered | Yes | Yes | - |
| Memory cards | Cards display | They have identical dimensions and are arranged in a grid layout. Initially, they appear "closed" with a white background. A hover effect is applied, and the cursor changes to indicate that they are clickable.| Yes | Yes | - |
| Game logic | Game logic | The images are revealed only when clicked. Once a card is clicked, it becomes disabled and cannot be clicked again. After the user clicks two cards, they are re-enabled for further interactions. Each time the user clicks two cards, the "moves" count increases by 1. However, the "score" only increases by 100 when a match is made. The player wins once their score reaches 800 | Yes | Yes | - |
| Restart Game button | Restarts the game | It restarst the game at any time | Yes | Yes | - |
| Restart Game button | Hover over them | The button will rotate slightly and change colors to a gradient of blue and purple | Yes | Yes | - |
| **Game Finished Congratulations Page** | | | | | |
| Header | Game name display | The title is centered and positioned as the topmost element on the page and it is readable | Yes | Yes | - |- |
| Game Finished - Congratulations Page | Page displays | This page appears 4s after the player has won | Yes | Yes | - |
| Congratulations text | Text display | The paragraph stands out, the content is centered with no spelling mistakes | Yes | Yes | - |
| Home Menu button | Click on the Home Menu button | edirects to the Home Menu page | Yes | Yes | - |
| Play Again! button | Click on the Play Again! button | Redirects to the Memory Board Game page | Yes | Yes | - |
| Both buttons | Hover over them | The buttons will rotate slightly and change colors to a gradient of blue and purple | Yes | Yes | 
| Both buttons | Buttons displayed | The buttons are centered one of top of the other with a consisting style, and they are readable | Yes | Yes | 

---
## Browser compatibility

The website was tested on the following browsers:
- Google Chrome
- Firefox
- Microsof Edge

---
## Bugs
+ ### Solved bugs
  1. The W3C Markup validation detected the below error in the HTML code:
  ![bug HTML code](documentation/bugs/bug-error-html-code.png)
        - Solution: this mistake was spotted and corrected. 

  2. The W3C Markup validation detected the below warnings in the HTML code:
    ![warnings HTML code](documentation/bugs/bug-warnings-html-code.png)
      - Solution: To enhance the HTML syntax, a hidden H2 heading was added to each section without an existing heading.

  3. JSHint showed the following warning:
    ![warnings JS code](documentation/bugs/bug-warning1-jshint.png)
      - Solution: Although the original code was functioning correctly, the event listener logic was updated to avoid any potentially confusing semantics. A separate click handler function was created. This change ensures the correct card index is captured using a closure for the handleCardFlip function.

+ ### Unfixed bugs

  1. JSHint showed the following warning:

    ![warnings JS code](documentation/bugs/bug-warning2-jshint.png)
    
    - As described in the "Features left to implement" section, due to time constraints, I used onclick in all buttons of the HTML document for faster implementation. However, I recognize that mixing structure (HTML) with functionality (JS) is not best practice, as it can make the code harder to maintain and does not facilitate collaboration in team environments. After the project is graded, I plan to refactor the code by removing inline onclick attributes, and instead handling events via JavaScript by adding event listeners, ensuring better separation of concerns and improving maintainability.
  
---
## Deployment

The website has been deployed to GitHub pages following these steps:

1. In the GitHub repository for The Cosmic Match Memory Game [GitHub repository](https://github.com/ParedesGab/PP2-the-cosmic-match-memory-game), select the "Settings" tab.

2. Click on "Pages" from the field "Code and automation" (on the left), and select the below settings:
    - Source: deploy from a branch.
    - Branch: main.
    - click "Save".

3. Select the "Code" tab and refresh the page. 

4. On the right side of the page, a "Deployments" section has been activated indicating a successful deployment. 

5. The live link can be accessed [here](https://paredesgab.github.io/PP2-the-cosmic-match-memory-game/).

## Local Deployment

### Forking

To have a copy of the project in your repositories:
1. Log in or sign up to GitHub.
3. Navigate to the [project repository](https://github.com/ParedesGab/PP2-the-cosmic-match-memory-game).
4. In the top right corner, click the "Fork" button.
5. A new page titled "Create a new fork" will appear. Optionally, you can edit the repository name.
6. At the bottom of the page, click "Create fork."

### Cloning

1. Log in or sign up to GitHub.
2. Go to the [project repository](https://github.com/ParedesGab/PP2-the-cosmic-match-memory-game).
3. Click the green button "Code" and choose your preferred cloning method (for example: HTTPS, SSH, or GitHub CLI) and copy the provided url.
4. Open the terminal in your preferred code editor and change the current working directory to the one where you want the cloned directory
5. Run git clone in the terminal, paste the copied link, and press Enter.

---
## Credits 

### Content 

- The Code institute ci-full-template was used to create the GitHub repository of the Cosmic Match Memory Game website.

- [W3 Schools](https://www.w3schools.com/jsref/met_win_settimeout.asp) showed me how to use the setTimeout() method. 

- [W3 Schools](https://www.w3schools.com/jsref/prop_html_id.asp) showed me how to return the id property. 

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) showed me how to create elliptical corner radius used in the Control Area of the Memory Board Game section.

- I got further clarificaion on the used of Parameters vs Arguments from the from the YouTube channel [Anna McDougall](https://www.youtube.com/watch?v=5o4P8lESTF0).

- Stack Overflow solutions was also used to resolve doubts.

- Text was checked with DeepL Write for spelling mistakes. 

- I learned how to add other pages (e.g., home menu page, games indications and congratulations pages) with Javascript by reading the project of [Kristyna Wach](https://github.com/Cushione/four-seasons-memory-game) and testing it myself within my javascript code.

- Inspiration for memory game logic comes from the YouTube Channels [developedbyed](https://www.youtube.com/watch?v=-tlb4tv4mC4&t=3095s) and [Victor Talamantes](https://www.youtube.com/watch?v=c0eigGnotm0). However, I did  not relied on them and customized it my way.

- ReadMe was inspired and guided by the ReadMe documents of my mentor Iuliia Konovalova, of my previous Kamil Wojciechowski, and of the love running project. 

### Media
  
- The universe background image is from [Federico Beccari](https://unsplash.com/de/@federize?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash).

- All memory card images are from [Icongeek26](https://www.flaticon.com/authors/icongeek26).

## Acknowledgments

- My sincere gratitude to my mentor, Iuliia Konovalova, for her valuable feedback.  
- Thank you to Code Institute, specially to Kamil, Kristyna, and Lane for the great tips and feedback.
- Thank you to my brother Brando, Your beautiful piano music [Brando PR](https://www.youtube.com/@BrandoPR) accompanied me along this project as well.
- I am deeply grateful to Geddi and Alexis for their insightful JavaScript fundamentals guidance.
- A heartfelt thanks to my husband Johannes for "playing! (testing)
 the game more times than I can count. 
