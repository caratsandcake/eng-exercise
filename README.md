# Carats and Cake Engineering Exercise

Carat's product team manages both the business and customer facing features of our payments platform. At the core of our work is the understanding and implementation of full stack web development principles and best practices.

We've designed this take home to get a sense of how you think and work as a developer. There is no one way to solve for the prompt below, but make sure to read this document thoroughly to understand how to succeed.

## Before you start

We are not trying to make you work for free, so please do not spend more than four hours on this exercise. If you find yourself needing more time, message your hiring contact and they can help you scope down your work to ensure you are not putting in more time than necessary.

Optionaly, feel free to write a `TODO.txt` doc of things you would have liked to get to with more time.

## Choosing your tech stack

Our application is built in React, Rails, and Postgres with a mix of dependencies you would likely expect for an app working on payment processing.

For this exercise do not feel beholden to our tech stack, but be ready to walk us through your code and explain your decision making process.

The only thing we will prescribe is that you use the [Stripe Checkout API](https://stripe.com/docs/payments/checkout) to handle the actual payment processing - everything else should be built by you.

## Prompt

You will be building a lightweight invoicing application. This application should allow a user to:
1. View a list of all existing invoices.
2. Create a new invoice.
3. Edit or delete any invoice.
4. Pay an outstanding invoice using Stripe checkout.
5. Check the status of a single invoice.

In our scenario we don't need line items on the invoice, feel free to just use a `total_amount` type column.

## Requirements

Your application should include the following:
1. A frontend form that takes user input and makes a request with that data
  -- Feel free to use the pre-built Stripe Checkout form for this functionality, but this is purely optional for time, not a requirement.
2. A web server that receives form HTTP request and uses customer data to make payment request to the Stripe Checkout API
3. A db instance or lightweight, model pattern based, data store for persisting any necessary invoice data to fulfill prompt success criteria.


## Getting started
1. Fork this repo to begin the exercise.
2. [Create a free Stripe account](https://dashboard.stripe.com/register) - your `Test mode` API credentials will be on [this page](https://dashboard.stripe.com/test/dashboard) once signup flow completes.
3. Please keep both the frontend and web server in this monorepo for us to review.
4. Use the Stripe Checkout API docs [here](https://stripe.com/docs/payments/checkout) to get started with the API.
5. When done, send your hiring contact a link to your forked version of this repository with your work.

*For testing payments, please see the Stripe testing page [here](https://stripe.com/docs/testing).*

## Details
- When landing on the page, a user should see a form prompting them for their billing info, contact info, and payment information.
- If a user tries to pay with a credit card and for whatever reason it cannot be successfully processed (example: `insufficient funds`) they should be alerted to that reason and be able to correct their entry before re-submitting.
- On successful payment the user should be redirected to a success message screen with any relevant information.

## Suggestions

- Add the amount of test coverage you feel is appropriate for the scope of this application (and be prepared to talk to testing choices made).

- Do not spend time on implementing authentication (we care about general data modeling and persistence best practices - not auth pattern implementation).

- Your frontend does not have to be responsive (we will be testing your code on desktop only).

- If you choose to use React: we use functional components over classes, and [hooks](https://reactjs.org/docs/hooks-intro.html) where necessary.

- You can use any data fetching library you like (`fetch`, `axios`, or other).

- This exercise is meant to get a sense of you as a programmer, so when relevant please let us know in comments about the choices you made, and why.

- Regardless of tech stack, be prepared to speak to the considerations you made around code reliability and readability.

- It always helps if your frontend looks at least slightly considered, but do not spend the bulk of your time on styling (we use Bootstrap 5 as an easy option).
