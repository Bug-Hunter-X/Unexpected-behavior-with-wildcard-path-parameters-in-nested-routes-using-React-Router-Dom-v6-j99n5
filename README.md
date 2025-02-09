# React Router Dom v6 Issue with Nested Routes and Wildcard Path Parameters

This repository demonstrates an unexpected behavior in React Router Dom v6 when using nested routes with a wildcard path parameter.  The issue occurs when navigating to a path that matches the wildcard, but also contains additional path segments.  In this scenario, the component associated with the wildcard route may not render correctly. The issue seems to be related to how React Router handles wildcard matches within a nested route structure.

## Steps to Reproduce
1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the application using `npm start`.
4. Navigate to `/contact`. The contact component renders correctly.
5. Navigate to `/contact/details` or any other path under `/contact`. The Contact component does not render as expected (sometimes it renders nothing).

## Expected Behavior
The Contact component should render when navigating to any path under the `/contact` route (e.g., `/contact`, `/contact/details`, `/contact/support`).

## Actual Behavior
The Contact component does not render when navigating to paths like `/contact/details`.