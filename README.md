# 💈 Barbering Appointment System

A modern, full-stack appointment booking application for barbershops built with Next.js, React, and TypeScript. This platform enables seamless scheduling for both barbers and clients with an intuitive interface and comprehensive management features.

---

## 🎯 Features

### For Clients
- **Easy Appointment Booking** - Book appointments with your preferred barber
- **Service Selection** - Choose from available barbershop services
- **Appointment Reminders** - Get notifications for upcoming appointments
- **Service Reviews** - Leave ratings and reviews for services
- **View History** - Track past and upcoming appointments
- **Gallery Browsing** - Explore barbershop portfolio and work samples

### For Barbers
- **Client Management** - View and manage all clients
- **Appointment Dashboard** - Comprehensive appointment scheduling and tracking
- **Service Management** - Create and manage service offerings
- **Gallery Management** - Post and manage portfolio images
- **Client Review System** - Monitor client feedback and ratings

### General
- **User Authentication** - Secure login and registration system
- **Context-based State Management** - Efficient state handling with React Context
- **Responsive Design** - Mobile-first approach with Tailwind CSS
- **Form Validation** - Robust client-side validation with Zod and React Hook Form
- **Toast Notifications** - User feedback via toast messages

---

## 🛠️ Tech Stack

### Frontend
- **Next.js 15.1.6** - React framework with App Router
- **React 19** - UI library
- **TypeScript 5** - Type safety
- **Tailwind CSS 3.4** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives
- **React Hook Form 7.54** - Efficient form management
- **Zod 3.24** - Schema validation
- **Axios 1.7.9** - HTTP client
- **Lucide React** - Modern icon library

### Development Tools
- **ESLint 9** - Code linting
- **PostCSS 8** - CSS processing
- **Turbopack** - Next.js bundler optimization

---

## 📁 Project Structure

```
src/
├── app/                              # Next.js App Router
│   ├── globals.css                   # Global styles
│   ├── layout.tsx                    # Root layout
│   ├── page.tsx                      # Home page
│   ├── (Auth)/                       # Auth routes (grouped)
│   │   ├── Login/                    # Login page
│   │   │   ├── page.tsx
│   │   │   ├── hook/
│   │   │   │   └── useLoginForm.ts
│   │   │   └── utils/
│   │   │       └── loginForm.ts
│   │   └── SignUp/                   # Registration page
│   │       ├── page.tsx
│   │       ├── hook/
│   │       │   └── useSignUp.ts
│   │       └── utils/
│   │           └── signup.ts
│   ├── Dashboard/                    # Protected dashboard routes
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── Barber/                   # Barber-specific views
│   │   │   ├── page.tsx
│   │   │   ├── All-Client/
│   │   │   ├── Appiontments/
│   │   │   ├── Post-Gallery/
│   │   │   └── Services-post/
│   │   └── User/                     # Client-specific views
│   │       ├── page.tsx
│   │       ├── Reminder/
│   │       ├── Reviews/
│   │       └── Servicess/
│   ├── Components/                   # Feature components
│   │   ├── browserSerCarousel.tsx
│   │   ├── Gallery.tsx
│   │   ├── Reviews.tsx
│   │   ├── Sidebar.tsx
│   │   └── Form/
│   │       ├── form.tsx
│   │       ├── hook/
│   │       └── utils/
│   ├── context/
│   │   └── AuthContext.tsx           # Authentication context
│   └── Shared/
│       ├── GenericForminput.tsx
│       └── API/
│           └── Request.ts             # API utilities
├── components/                        # UI component library
│   └── ui/                            # shadcn/ui components
│       ├── button.tsx
│       ├── carousel.tsx
│       ├── form.tsx
│       ├── input.tsx
│       ├── label.tsx
│       ├── select.tsx
│       ├── tabs.tsx
│       ├── textarea.tsx
│       └── toast.tsx
├── hooks/
│   └── use-toast.ts                   # Toast notification hook
└── lib/
    └── utils.ts                       # Utility functions
```

---

## 🚀 Getting Started

### Prerequisites
- **Node.js** 18.0 or higher
- **npm**, **yarn**, **pnpm**, or **bun** package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd barbering-appointment
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   ```bash
   NEXT_PUBLIC_API_URL=http://localhost:3001
   # Add other required environment variables
   ```

4. **Run the development server**
   ```bash
   npm run dev
   ```
   
   Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

---

## 📝 Available Scripts

- **`npm run dev`** - Start development server with Turbopack
- **`npm run build`** - Build for production
- **`npm start`** - Start production server
- **`npm run lint`** - Run ESLint to check code quality

---

## 🔐 Authentication

The application uses a context-based authentication system with `AuthContext.tsx` to manage user sessions. 

- **Login Page** - `/auth/login` - Existing users can sign in
- **Sign Up Page** - `/auth/signup` - New users can register
- **Protected Routes** - Dashboard routes are protected and require authentication

---

## 🎨 UI Components

Custom UI components built with:
- **Radix UI** - For accessible primitives
- **Tailwind CSS** - For styling
- **shadcn/ui** - Pre-built component library

Components include buttons, inputs, forms, carousels, tabs, and toast notifications.

---

## 📡 API Integration

API requests are handled through:
- **Axios** - HTTP client for API calls
- **Request.ts** - Centralized API request utilities
- **React Hook Form** - Form state management
- **Zod** - Schema validation

---

## 🧪 Form Validation

Forms use a combination of:
- **React Hook Form** - Efficient form handling
- **Zod** - Runtime schema validation
- **Custom hooks** - Reusable form logic (e.g., `useLoginForm`, `useSignUp`)

---

## 📱 Responsive Design

The application is built with a mobile-first approach using:
- **Tailwind CSS** - Utility-based responsive design
- **Responsive layouts** - Adapts to all screen sizes
- **Image optimization** - AVIF format images in public folder

---

## 🎯 Core Functionalities

### Authentication Flow
1. Users register via Sign Up
2. Credentials are validated
3. Authentication state managed via Context
4. Protected routes accessible after login

### Appointment Booking
1. Client selects service and date
2. Form validation via Zod + React Hook Form
3. Appointment stored in system
4. Confirmation displayed via toast

### Dashboard
- **Barber Dashboard** - Manage clients, appointments, services, gallery
- **Client Dashboard** - View appointments, reminders, reviews, services

---

## 🚀 Deployment

### Deploy to Vercel (Recommended)

1. Push your code to GitHub
2. Visit [Vercel Dashboard](https://vercel.com)
3. Create new project from GitHub repository
4. Set environment variables
5. Deploy

### Deploy Elsewhere

```bash
npm run build
npm start
```

---

## 📚 Learning Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [React Documentation](https://react.dev)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Radix UI](https://www.radix-ui.com/docs/primitives/overview/introduction)

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 📞 Support

For support, questions, or feedback, please open an issue in the repository or contact the development team.

---

**Made with ❤️ for barbershops and their clients**
