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

## Getting started
1. Create a new project repo, separate from this one. Please keep project in a monorepo for ease of review.  
2. [Create a free Stripe account](https://dashboard.stripe.com/register) - your `Test mode` API credentials will be on [this page](https://dashboard.stripe.com/test/dashboard) once signup flow completes.
3. Please keep both the frontend and web server in this monorepo for us to review.
4. Use the Stripe Checkout API docs [here](https://stripe.com/docs/payments/checkout) to get started with the API.
5. When done, send your hiring contact a link to your project repository.

*For testing payments, please see the Stripe testing page [here](https://stripe.com/docs/testing).*

## Suggestions

- Add the amount of test coverage you feel is appropriate for the scope of this application (and be prepared to talk to testing choices made).

- Do not spend time on implementing authentication (we care about general data modeling and persistence best practices - not auth pattern implementation).

- Your frontend does not have to be responsive (we will be testing your code on desktop only).

- If you choose to use React: we use functional components over classes, and [hooks](https://reactjs.org/docs/hooks-intro.html) where necessary.

- You can use any data fetching library you like (`fetch`, `axios`, or other).

- This exercise is meant to get a sense of you as a programmer, so when relevant please let us know in comments about the choices you made, and why.

- Regardless of tech stack, be prepared to speak to the considerations you made around code reliability and readability.

- It always helps if your frontend looks at least slightly considered, but do not spend the bulk of your time on styling (we use Bootstrap 5 as an easy option).
