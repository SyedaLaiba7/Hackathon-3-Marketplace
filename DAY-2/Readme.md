# Project Overview

**FoodTuck** is a modern and responsive e-commerce platform tailored for food delivery, offering a specialized marketplace for quick commerce food items. Built with innovative technologies, the platform ensures a seamless shopping experience for food lovers.

The project leverages **Sanity CMS** for efficient content management and **Next.js** for a dynamic and scalable frontend, ensuring smooth interaction between backend systems and the user interface. Key features include real-time menu updates, order tracking, intuitive navigation, and secure payment integrations.

The vision for FoodTuck is to become the go-to platform for food truck enthusiasts, combining cutting-edge technology with a user-friendly design. This project highlights scalability, efficiency, and a food-first approach, providing a unique and comprehensive ordering experience. 🚀

## Day 2: Planning the Technical Foundation

### System Architecture

Here’s the high-level system architecture diagram illustrating how the components interact:

- **Frontend (Next.js)**: The user interface for browsing menus and placing orders.
- **Sanity CMS**: Acts as the backend, managing data like food truck menus, orders, and customer information.
- **Product Data API**: Fetches food truck menu details from Sanity CMS for dynamic display on the frontend.
- **Third-Party API**: Handles integrations like shipment/order tracking and payment processing.
- **Order Tracking API**: Fetches real-time order delivery status.
- **Payment Gateway**: Processes payments securely and sends payment confirmations back to Sanity CMS.

### Key Workflow Steps

#### Menu Browsing

- The frontend requests menu items via the Product Data API connected to Sanity CMS.

#### Order Placement

- The user places an order; details are sent to Sanity CMS via an API request.

#### Order Tracking

- Order delivery status is fetched through the Third-Party API and displayed on the frontend.

### Technologies

#### Frontend

- **Next.js**: For building server-rendered, dynamic UIs.
- **Tailwind CSS**: For responsive and beautiful designs.
- **Shadcn/UI**: For customizable UI components.

#### Backend

- **Sanity CMS**: To manage and structure content effectively.
- **Clerk**: For user authentication and management.

#### APIs

- **ShipEngine API (Optional)**: For tracking delivery of food orders.
- **Stripe API**: For secure and seamless payment processing.

#### Tools

- **GitHub**: For version control and collaboration.
- **Postman**: To test and document APIs.
- **Vercel**: For fast and reliable deployment.

### API Endpoints

| Endpoint                        | Method | Description                                      |
|---------------------------------|--------|--------------------------------------------------|
| `/api/create-order`             | POST   | Creates a new order when someone buys food.      |
| `/api/orders`                   | GET    | Fetches all orders (admin functionality).        |
| `/api/track-orders`             | GET    | Lets users see all of their orders.              |
| `/api/send/confirmation-email`  | POST   | Sends an email to confirm an order.              |
| `/api/reviews/:productId`       | POST   | Adds a review for a menu item.                   |
| `/api/reviews/:productId`       | GET    | Fetches reviews for a menu item.                 |
| `/api/menu-items`               | GET    | Retrieves food menu items dynamically from Sanity CMS. |

### API Documentation

#### Add a Review for a Food Item

- **Endpoint**: `/api/reviews/:productId`
- **Method**: POST
- **Description**: Adds a review for a specific food item.
- **Parameters**:
    - `productId` (String): The unique identifier of the food item.
    - `content` (String): Review content provided by the user.
    - `rating` (Number): A numeric rating for the food item.

### Sanity and Next.js Interaction

Sanity CMS is integrated into the Next.js application to provide dynamic and flexible content management. The interaction works as follows:

#### Data Management in Sanity

- All food-related data (e.g., menus, orders, and customers) is stored and managed in Sanity's content studio.

#### Fetching Data

- Next.js fetches data from Sanity using GROQ queries via Sanity's API endpoints. These queries retrieve structured content.

#### Rendering Components

- The fetched data is passed to React components for rendering dynamic and interactive user interfaces.

#### Real-Time Updates

- Sanity's webhooks notify the application of changes (e.g., menu updates), enabling immediate updates without manual rebuilds.

#### Page Types

- **Server-side Rendering (SSR)**: For dynamic pages like food item details and order details.
- **Static Site Generation (SSG)**: Pages like home, category, and menu pages are pre-rendered at build time.

## Conclusion

Day 2 focused on laying the technical foundation for FoodTuck, transitioning from ideation to actionable planning. By defining technical requirements, designing a robust system architecture, and planning API integrations, we established a clear roadmap for development.

As we move forward, our focus will shift to coding, testing, and delivering a functional and scalable solution that offers a seamless food-ordering experience. By adhering to the submission guidelines and maintaining collaboration, we are confident in achieving project success! 🚀