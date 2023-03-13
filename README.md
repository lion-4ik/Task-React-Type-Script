# MMHG Typescript React Exercise 1

**When complete, submit a PR / push your changes to this repository.**

**Candidates completing this exercise are welcome to refer to online references (e.g., Stack Overflow), but not to post content from this assignment. We ask that you do not act in such a way that would constitute cheating, misrepresentation, or unfairness.**


## Overview

This project is a simple React webapp. It is a fictional physician portal for "Good Health Clinic" that consists of a Patient List page and an About Us page.

The project uses React Router for routes and MobX for state. Every time the webapp is loaded, it loads the content of `src/server/Patient/data/SamplePatientData.ts` into the PatientListState store.

The project has been confirmed to run as expected with Node.js version 16.x.


## Exercise

1. Add a dropdown to the top of the Patient List page that allows the user to change how the patient list is sorted.
   
   #### Requirements
   
   i. There should be six options in the dropdown: Patient ID (Ascending), First Name (Ascending), Last Name (Ascending), Patient ID (Descending), First Name (Descending), and Last Name (Descending).
   
   ii. The patient list should update immediately after the dropdown value is changed.
   
   iii. The dropdown selection should be preserved if the user navigates to another page in the webapp (e.g., About Us) and then back to the Patient List (it does not need to be preserved if the webapp is reloaded).


2. Both the Patient List and About Us pages use the same `Header` component to display a header at the top of the page. React Router 6 supports a new feature called **Outlets** that allows a parent route to render their child route elements. Refactor the Patient List and About Us pages to add a new parent route that renders the `Header` component and uses an `Outlet` to render the Patient List or About Us page content.


3. Add a new Patient page that allows a single patient to be edited. The page has the following requirements.
   
   #### Requirements
   
   i. The page should display the same header that is shown on the other pages.
   
   ii. The page should display the following values from the patient and allow them to be edited: ULI, firstName, lastName, birthDate, height, and weight.
   
   iii. The page should validate user inputs and only accept sensible values, particularly for dates and numbers.
   
   iv. There should be a "Save" button at the bottom that saves the updated values for the patient and takes the user to the patient list page. The updated values should be reflected in the patient list page.
   
   v. The page should be added as a route with React Router. The page should use a sensible path in the browser (i.e., the path should probably include some value that uniquely identifies the patient).
   
   vi. The page should be able to be navigated to by clicking on a row in the patient list, or by navigating directly to the page using the path in the browser.
