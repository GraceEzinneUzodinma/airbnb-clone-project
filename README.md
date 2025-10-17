# airbnb-clone-project
## Team Roles
### Backend Developer
Responsible for building and maintaining the server-side logic, APIs, and business logic. Handles data processing, authentication, and integration with the database.
### Frontend Developer
Focuses on creating the user interface and user experience. Builds responsive web pages, handles client-side logic, and ensures the application is user-friendly and visually appealing.
### Database Administrator
Manages the database structure, optimization, and data integrity. Ensures data is stored securely and efficiently, and handles backups and recovery.
### Project Manager
Oversees the project timeline, coordinates team members, manages resources, and ensures the project stays on track and meets objectives.
### QA/Tester
Tests the application to identify bugs and issues before deployment. Ensures the product meets quality standards and works as expected. 
## Technology Stack

### Frontend
- **HTML**: Markup language for creating the structure and content of web pages.
- **CSS**: Styling language for designing the layout, colors, and visual appearance of the application.
- **JavaScript**: Programming language for adding interactivity and dynamic behavior to the frontend.
- **React** (Optional): A JavaScript library for building interactive user interfaces with reusable components.

### Backend
- **Node.js**: JavaScript runtime environment that allows you to run JavaScript on the server side.
- **Express**: A lightweight web framework for Node.js that simplifies building RESTful APIs and handling HTTP requests.

### Database
- **MongoDB**: A NoSQL database that stores data in JSON-like documents, providing flexibility and scalability for the application.

### Additional Technologies
- **Git**: Version control system for tracking changes and collaborating on code.
- **GitHub**: Platform for hosting and managing Git repositories and team collaboration.
## Database Design

### Key Entities

#### Users
- **user_id**: Unique identifier for each user
- **name**: Full name of the user
- **email**: Email address for login and communication
- **password**: Encrypted password for authentication
- **phone**: Contact phone number

#### Properties
- **property_id**: Unique identifier for each property
- **owner_id**: Foreign key linking to the user who owns the property
- **title**: Name/title of the property
- **description**: Detailed description of the property
- **location**: Address and coordinates of the property
- **price_per_night**: Nightly rental rate

#### Bookings
- **booking_id**: Unique identifier for each booking
- **user_id**: Foreign key linking to the user making the booking
- **property_id**: Foreign key linking to the property being booked
- **check_in_date**: Date when the guest checks in
- **check_out_date**: Date when the guest checks out
- **total_price**: Total cost of the booking

#### Reviews
- **review_id**: Unique identifier for each review
- **user_id**: Foreign key linking to the user who wrote the review
- **property_id**: Foreign key linking to the property being reviewed
- **rating**: Numerical rating (1-5 stars)
- **comment**: Text feedback from the reviewer

#### Payments
- **payment_id**: Unique identifier for each payment
- **booking_id**: Foreign key linking to the booking being paid for
- **amount**: Payment amount
- **payment_date**: Date when the payment was made
- **payment_method**: Method used (credit card, PayPal, etc.)

### Entity Relationships
- A **User** can own multiple **Properties** (one-to-many relationship)
- A **User** can make multiple **Bookings** (one-to-many relationship)
- A **Property** can have multiple **Bookings** (one-to-many relationship)
- A **Booking** is linked to one **Payment** (one-to-one relationship)
- A **Property** can have multiple **Reviews** (one-to-many relationship)
- A **User** can write multiple **Reviews** (one-to-many relationship)