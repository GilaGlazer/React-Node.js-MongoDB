# Event Management System 🎭

A comprehensive web application for managing events and connecting event producers with event seekers. This system provides separate interfaces for event producers to manage their events and for regular users to discover and explore events.

## 🎯 Project Overview

The Event Management System serves as a bridge between event producers and consumers, offering:
- **Event Producers**: Complete event and profile management capabilities
- **Event Seekers**: Easy event discovery and detailed information access
- **Clean Architecture**: Separation of concerns with dedicated interfaces for different user types

## 👥 Target Users

- **Event Producers**: Creators and organizers of programs and events
- **Event Seekers**: People looking for events and programs to attend

## 🏗️ System Architecture

### Frontend (React + TypeScript)
- **Technology Stack**: React, TypeScript, Axios
- **Architecture**: Component-based modular design
- **User Interfaces**: Separate workflows for producers and seekers

### Backend (Node.js + Express)
- **Technology Stack**: Node.js, Express, MongoDB, Mongoose
- **API Design**: RESTful endpoints with proper HTTP methods
- **Database**: MongoDB with Mongoose ODM

## 🚀 Features

### Event Producer Interface
- **Producer Management**
  - Create new producer profiles
  - Update producer information
  - View existing producer details
- **Event Management**
  - Create new events
  - Edit existing events
  - Delete events
  - View event lists

### Event Seeker Interface
- **Event Discovery**
  - Browse all available events
  - Filter events by name
  - View detailed event information
- **Producer Information**
  - Access producer contact details
  - View producer profiles

## 🗂️ Component Structure

### Core Components
- `ProducerDetails` - Display and edit producer information
- `AddProducer` - Create new producer profiles
- `ProducerEventList` - List events for specific producers
- `EventDetails` - Event information with editing capabilities
- `AddEvent` - Create new events
- `EventList` - Browse events with filtering
- `UserEventDetails` - Read-only event information for seekers
- `MainMenu` - Primary navigation component
- `ProducerMenu` - Producer-specific navigation

## 🛠️ API Endpoints

### Producer Endpoints
```
GET    /producer/:email    # Get producer by email
POST   /producer           # Create new producer
PUT    /producer/:id       # Update producer details
```

### Event Endpoints
```
GET    /events             # Get all events
GET    /events/:id         # Get specific event
POST   /events             # Create new event
PUT    /events/:id         # Update event
DELETE /events/:id         # Delete event
```

## 📊 Database Schema

### Producers Collection
```javascript
{
  _id: ObjectId,
  name: String,
  email: String,
  phone: String,
  description: String
}
```

### Events Collection
```javascript
{
  _id: ObjectId,
  type: String,
  name: String,
  description: String,
  details: String,
  producerId: ObjectId (ref: Producer)
}
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm

## 🎨 User Interface Flow

### Homepage
- **Producer Login** - Access producer management features
- **User Login** - Browse events as a seeker

### Producer Workflow
1. Choose: Add New Producer or Existing Producer
2. Manage producer profile and contact information
3. View and manage event listings
4. Create, edit, or delete individual events

### User Workflow
1. Browse filtered event listings
2. Click events for detailed information
3. View producer contact details

## 🔧 Development Standards

- **Clean Code Practices**: Modular design with clear separation of concerns
- **TypeScript**: Strong typing for better code reliability
- **Component Architecture**: Reusable and maintainable React components
- **RESTful API**: Standard HTTP methods and status codes
- **Error Handling**: Proper error responses and user feedback

## 📝 Development Notes

This project focuses on core functionality and basic integration:
- ✅ Database connectivity and CRUD operations
- ✅ Frontend-backend integration
- ✅ Basic user interface implementation
- 🔄 Future enhancements: Authentication, advanced validation, security features

## 🤝 Contributing

This system is designed with scalability in mind. Future enhancements may include:
- User authentication and authorization
- Advanced search and filtering
- Event categories and tags
- Image upload capabilities
- Email notifications
- Event booking system

## 📞 Support

For questions or support regarding this Event Management System, please refer to the project documentation or contact the development team.

---

**Built with ❤️ using React, Node.js, TypeScript, and MongoDB**
