# Dog Refuge Website - Project Specification

## 1. Project Overview
A website to manage and showcase the operations of a dog refuge. It will include:
- **Public Features**: Information about available dogs, adoption process, and volunteer opportunities.
- **Admin Features**: Management of dogs, employees, and volunteers via a dashboard.

---

## 2. Core Features

### Public Features
1. **Homepage**
   - Welcome message and overview of the refuge.
   - Call-to-action buttons for "Adopt a Dog" and "Volunteer with Us."

2. **Adoptable Dogs**
   - List of all available dogs with:
     - Name, age, breed, description, and photo.
     - A button to view more details about a specific dog.
   - Search and filter functionality (e.g., by age, breed).

3. **Adoption Process**
   - Step-by-step explanation of the adoption process.
   - Contact form to apply for adoption.

4. **Volunteer Page**
   - Information on how to volunteer.
   - Online application form for potential volunteers.

5. **About Us**
   - Information about the refuge's mission, history, and team.

6. **Contact Page**
   - Contact form with fields for name, email, phone, and message.
   - Location with an embedded map and contact details.

### Admin Features
1. **Admin Dashboard**
   - Secure login system for employees.
   - Overview panel with quick stats (e.g., total dogs, employees, and volunteers).

2. **Dog Management**
   - Add, update, or delete dog profiles.
   - Upload and manage photos for dogs.

3. **Employee Management**
   - Add, update, or delete employee records.
   - Assign roles (e.g., admin, caretaker).

4. **Volunteer Management**
   - Add, update, or delete volunteer records.
   - Track volunteer applications.

5. **Adoption Requests**
   - List of adoption requests.
   - Mark requests as "approved," "pending," or "declined."

---

## 3. Technology Stack
- **Backend**: Express.js
- **Database**: MariaDB
- **Frontend**: React.js with TypeScript
- **Styling**: Sass
- **Other Tools**:
  - Node.js for running the backend.
  - Vite for bundling the React frontend.
  - Git for version control.
  - Docker for deployment

---

## 4. Database Design

### Tables:

1. **Dogs**
   - `ID` (Primary Key)
   - `Name`
   - `Age`
   - `Breed`
   - `Description`
   - `Photo URL`
   - `Adoption Status` (Available/Adopted)

2. **Employees**
   - `ID` (Primary Key)
   - `Name`
   - `Role`
   - `Email`
   - `Phone`

3. **Volunteers**
   - `ID` (Primary Key)
   - `Name`
   - `Email`
   - `Phone`
   - `Application Status` (Approved/Pending/Declined)

4. **Adoption Requests**
   - `ID` (Primary Key)
   - `Dog ID` (Foreign Key)
   - `Adopter Name`
   - `Adopter email`
   - `Adopter phone`
   - `Request Status` (Approved/Pending/Declined)

5. **Credentials**
	- `User ID` (Foreign Key)
	- `User Name`
	- `Password Hash`

---

## 5. Development Milestones

### Month 1: Setup and Foundations
- **Week 1**: Project setup (Express server, MariaDB database, and React frontend).
- **Week 2**: Create database schema and initial API routes (e.g., CRUD for dogs).
- **Week 3**: Build basic frontend structure (React components, Sass setup).
- **Week 4**: Implement homepage and dog listing page (frontend-backend integration).

### Month 2: Core Features
- **Week 1**: Develop dog management system (admin dashboard).
- **Week 2**: Add employee and volunteer management features.
- **Week 3**: Implement adoption request handling.
- **Week 4**: Style all pages and components with Sass.

### Month 3: Testing and Deployment
- **Week 1**: Test API routes and database functionality.
- **Week 2**: Add authentication for admin dashboard.
- **Week 3**: Finalize frontend and polish UX/UI.
- **Week 4**: Deploy the application (e.g., on Vercel/Netlify for frontend, Railway/Render for backend).

---

## 6. Additional Considerations

### Security
- Sanitize and validate user input.
- Use environment variables for sensitive information (e.g., database credentials).
- Secure the admin dashboard with authentication and role-based access.

### Scalability
- Design APIs to allow future features like donations or event management.

### Documentation
- Document APIs, database schema, and project structure.

### Testing
- Write unit and integration tests for backend routes.
- Test frontend functionality and responsiveness.
