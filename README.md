# Connect - Local Service Finder App

A modern, responsive web application for connecting users with local service providers. Built with Next.js, Firebase, and Tailwind CSS with a classic royal blue and gold theme.

## 🌟 Features

### For Users
- **Search Services**: Find local service providers by category and location
- **Browse Categories**: Explore services like Electrician, Barber, Cab, Plumber, etc.
- **Contact Providers**: Direct contact with service providers via phone
- **Responsive Design**: Works seamlessly on desktop and mobile devices

### For Service Providers
- **Easy Registration**: Simple form to register as a service provider
- **Category Selection**: Choose from multiple service categories
- **Location-based Listing**: Specify service areas for better visibility

### For Administrators
- **Provider Management**: Review and approve new provider registrations
- **Status Tracking**: Monitor pending, approved, and rejected providers
- **Delete Functionality**: Remove inappropriate or inactive providers

## 🎨 Design Features

- **Royal Theme**: Classic royal blue (#273c75) and gold (#f1c40f) color scheme
- **Modern UI**: Clean, professional design with soft shadows and rounded elements
- **Responsive Layout**: Mobile-first design that works on all screen sizes
- **Accessibility**: Proper ARIA attributes and keyboard navigation support

## 🚀 Tech Stack

- **Frontend**: Next.js 15.3.2 with React 19
- **Styling**: Tailwind CSS with custom royal theme
- **UI Components**: Shadcn/ui component library
- **Backend**: Firebase Firestore for database
- **Authentication**: Firebase Auth (ready for implementation)
- **Maps**: Google Maps API integration
- **TypeScript**: Full type safety throughout the application

## 📁 Project Structure

```
src/
├── app/
│   ├── layout.tsx              # Root layout with theme
│   ├── page.tsx                # Homepage with search and categories
│   ├── providers/
│   │   └── page.tsx            # Provider listings with filters
│   ├── register-provider/
│   │   └── page.tsx            # Provider registration form
│   └── admin/
│       └── page.tsx            # Admin panel for provider management
├── components/
│   ├── ui/                     # Shadcn UI components
│   ├── SearchBar.tsx           # Search functionality
│   ├── CategoryCard.tsx        # Service category display
│   ├── ProviderCard.tsx        # Provider information card
│   └── Map.tsx                 # Google Maps integration
└── lib/
    ├── firebase.ts             # Firebase configuration
    └── utils.ts                # Utility functions
```

## 🛠️ Installation & Setup

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Firebase project
- Google Maps API key

### 1. Clone and Install
```bash
git clone <repository-url>
cd connect-app
npm install
```

### 2. Environment Configuration
Create a `.env.local` file in the root directory:

```env
# Firebase Configuration
NEXT_PUBLIC_FIREBASE_APIKEY=your-firebase-api-key
NEXT_PUBLIC_FIREBASE_AUTHDOMAIN=your-project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECTID=your-project-id
NEXT_PUBLIC_FIREBASE_STORAGEBUCKET=your-project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGINGSENDERID=your-messaging-sender-id
NEXT_PUBLIC_FIREBASE_APPID=your-app-id

# Google Maps API Key
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your-google-maps-api-key
```

### 3. Firebase Setup
1. Create a new Firebase project at [Firebase Console](https://console.firebase.google.com)
2. Enable Firestore Database
3. Set up the following Firestore collection:

```
providers/
├── {documentId}
│   ├── name: string
│   ├── phone: string
│   ├── category: string
│   ├── location: string
│   ├── status: 'pending' | 'approved' | 'rejected'
│   └── createdAt: timestamp
```

### 4. Google Maps Setup
1. Go to [Google Cloud Console](https://console.cloud.google.com)
2. Enable Maps JavaScript API
3. Create an API key and add it to your environment variables

### 5. Run the Application
```bash
npm run dev
```

Visit `http://localhost:8000` to see the application.

## 📱 Usage Guide

### For Users
1. **Search Services**: Use the search bar on the homepage to find services by type and location
2. **Browse Categories**: Click on category cards to filter providers
3. **Contact Providers**: Click the "Contact" button on provider cards to get phone numbers

### For Service Providers
1. **Register**: Click "Register as Provider" on the homepage
2. **Fill Form**: Complete the registration form with your details
3. **Wait for Approval**: Your registration will be reviewed by administrators
4. **Get Listed**: Once approved, you'll appear in search results

### For Administrators
1. **Access Panel**: Click "Admin Panel" on the homepage
2. **Review Registrations**: Check pending provider registrations
3. **Approve/Reject**: Use the action buttons to approve or reject providers
4. **Manage Providers**: Delete inappropriate or inactive providers

## 🔧 API Endpoints

The application uses Firebase Firestore for data management:

- **GET** `/providers` - Fetch approved providers
- **POST** `/providers` - Create new provider registration
- **PUT** `/providers/{id}` - Update provider status
- **DELETE** `/providers/{id}` - Delete provider

## 🎯 Key Features Implementation

### Search Functionality
- Real-time search by service type and location
- Filter providers by category and location
- URL-based search parameters for shareable links

### Provider Management
- Three-tier approval system (pending, approved, rejected)
- Admin controls for provider lifecycle management
- Automatic status tracking and timestamps

### Responsive Design
- Mobile-first approach with Tailwind CSS
- Consistent royal blue and gold branding
- Smooth animations and transitions

### Error Handling
- Comprehensive error boundaries
- User-friendly error messages
- Loading states for better UX

## 🚀 Deployment

### Vercel (Recommended)
```bash
npm run build
# Deploy to Vercel
```

### Other Platforms
The app can be deployed to any platform that supports Next.js:
- Netlify
- AWS Amplify
- Google Cloud Platform
- Self-hosted with Docker

## 🔒 Security Considerations

- Environment variables for sensitive data
- Firebase security rules (to be configured)
- Input validation and sanitization
- HTTPS enforcement in production

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the documentation
- Review Firebase and Next.js documentation

## 🔮 Future Enhancements

- User authentication and profiles
- Rating and review system
- Real-time chat between users and providers
- Payment integration
- Advanced search filters
- Mobile app development
- Multi-language support
- Analytics dashboard

---

**Connect** - Your trusted platform for finding local services. Built with ❤️ using modern web technologies.
