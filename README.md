# bddtask2

Feature: Login Action
    Description: This feature will test the login functionality on the Amazon website.

Scenario Outline: Login with valid and invalid credentials
    Given User is on Amazon Home Page
    When User navigates to Login Page
    Then User enters "<email>" and "<password>"
    And Keeping case as <Case>
    Then User should get logged in successfully if "<Case>" is valid
    And User should see the error message if "<Case>" is invalid
    Then User is redirected back to the login page and prompted to provide correct credentials if login is "<Case>"

Examples:
    | email                   | password      | Case    |
    | "mahasadha201@gmail.com" | "ssvm@4036" | Valid   |
    | "mahasdha@gmail.com" | "maha@1234" | Invalid |
