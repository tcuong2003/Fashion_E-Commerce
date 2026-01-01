# 🚀 Fashion E-Commerce

[![Next.js](https://img.shields.io/badge/Next.js-16.1.1-black)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19.2.3-blue)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.0-38B2AC)](https://tailwindcss.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-green)](https://mongoosejs.com/)
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black)](https://vercel.com/)

A modern, full-stack fashion e-commerce platform built with Next.js 16, featuring a sleek user interface, powerful admin dashboard, secure authentication, and optimized performance. Experience seamless shopping with real-time cart management, product browsing, and responsive design.

**🌐 Live Demo:** [https://fashion-e-commerce-smoky.vercel.app/](https://fashion-e-commerce-smoky.vercel.app/)

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Usage](#-usage)
- [Build & Deployment](#-build--deployment)
- [Project Structure](#-project-structure)
- [API Documentation](#-api-documentation)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)

---

## ✨ Features

### 🛍️ Customer Experience

- **Product Browsing**: Explore products by categories with advanced filtering and search
- **Product Details**: Detailed product pages with images, descriptions, and specifications
- **Shopping Cart**: Add/remove items, update quantities, and persistent cart across sessions
- **User Authentication**: Secure login/register with session management
- **Responsive Design**: Optimized for mobile, tablet, and desktop devices
- **Fast Navigation**: Leveraging Next.js App Router for instant page transitions

### 🛠️ Admin Dashboard

- **Product Management**: Create, read, update, and delete products with image uploads
- **User Management**: View and manage user accounts and orders
- **Category Management**: Organize products into categories
- **Blog Management**: Create and manage blog posts
- **Order Tracking**: Monitor and manage customer orders
- **Analytics**: Basic analytics and reporting features

### ⚡ Performance & Security

- **Image Optimization**: Automatic image compression and lazy loading
- **Server-Side Rendering**: Fast initial page loads with SSR
- **API Security**: Secure API routes with proper authentication
- **Database Optimization**: Efficient queries with Mongoose ODM
- **SEO Friendly**: Meta tags and structured data for better search visibility

---

## 🛠️ Tech Stack

### Frontend

- **[Next.js 16](https://nextjs.org/)** - React framework with App Router
- **[React 19](https://reactjs.org/)** - UI library
- **[TypeScript](https://www.typescriptlang.org/)** - Type-safe JavaScript
- **[TailwindCSS 4](https://tailwindcss.com/)** - Utility-first CSS framework
- **[Shadcn/UI](https://ui.shadcn.com/)** - Modern UI components built on Radix UI
- **[Lucide React](https://lucide.dev/)** - Beautiful icons
- **[Swiper](https://swiperjs.com/)** - Touch slider library

### Backend & Database

- **Next.js API Routes** - Serverless API endpoints
- **[Mongoose](https://mongoosejs.com/)** - MongoDB object modeling
- **[MongoDB](https://www.mongodb.com/)** - NoSQL database
- **[Argon2](https://github.com/ranisalt/node-argon2)** - Password hashing
- **[Axios](https://axios-http.com/)** - HTTP client

### DevOps & Tools

- **[Vercel](https://vercel.com/)** - Deployment platform
- **[Cloudinary](https://cloudinary.com/)** - Image hosting and optimization
- **[TinyMCE](https://www.tiny.cloud/)** - Rich text editor
- **[React Hook Form](https://react-hook-form.com/)** - Form management
- **[Zod](https://zod.dev/)** - Schema validation (if used)
- **[SASS](https://sass-lang.com/)** - CSS preprocessor

---

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (version 18 or higher)
- **npm**, **yarn**, or **pnpm** package manager
- **MongoDB** database (local or cloud instance like MongoDB Atlas)
- **Git** for version control

---

## 🚀 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/tcuong2003/Fashion_E-Commerce.git
   cd Fashion_E-Commerce
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Environment Setup**
   Create a `.env.local` file in the root directory and add the following variables:

   ```env
   MONGODB_URI=your_mongodb_connection_string
   NEXTAUTH_SECRET=your_nextauth_secret
   NEXTAUTH_URL=http://localhost:3000
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   ```

4. **Database Setup**

   ```bash
   # If using local MongoDB, make sure it's running
   # For MongoDB Atlas, ensure your connection string is correct
   ```

5. **Run the development server**

   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

---

## 📖 Usage

### For Customers

1. Browse products on the homepage
2. Use the search and filter options to find specific items
3. Click on products to view details
4. Add items to cart and proceed to checkout
5. Create an account or login to track orders

### For Admins

1. Navigate to `/admin` route
2. Login with admin credentials
3. Manage products, categories, users, and orders
4. Create blog posts and monitor analytics

---

## 🏗️ Build & Deployment

### Local Build

```bash
npm run build
npm run start
```

### Deploy to Vercel

1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically on push

### Docker Support

This project includes Docker support. See [DOCKER.md](./DOCKER.md) for detailed instructions.

---

## 📁 Project Structure

```
Fashion_E-Commerce/
├── app/                          # Next.js App Router pages
│   ├── (client)/                 # Client-side pages
│   │   ├── blogs/                # Blog pages
│   │   ├── cart/                 # Shopping cart
│   │   ├── contact/              # Contact page
│   │   └── products/             # Product pages
│   ├── admin/                    # Admin dashboard
│   ├── api/                      # API routes
│   └── globals.css               # Global styles
├── components/                   # Reusable React components
│   ├── ui/                       # Shadcn/UI components
│   ├── Header/                   # Header components
│   ├── ProductDetail/            # Product detail components
│   └── admin/                    # Admin-specific components
├── hooks/                        # Custom React hooks
├── lib/                          # Utility libraries
├── models/                       # Mongoose models
├── public/                       # Static assets
├── services/                     # API service functions
├── styles/                       # SCSS stylesheets
├── types/                        # TypeScript type definitions
├── utils/                        # Utility functions
├── package.json                  # Dependencies and scripts
├── next.config.ts                # Next.js configuration
├── tailwind.config.js            # TailwindCSS configuration
├── tsconfig.json                 # TypeScript configuration
└── README.md                     # Project documentation
```

---

## 📚 API Documentation

The API endpoints are organized as follows:

### Authentication

- `POST /api/auth/login` - User login

### Products

- `GET /api/products` - Get all products
- `POST /api/products` - Create product (Admin)
- `GET /api/products/[id]` - Get product by ID
- `PUT /api/products/[id]` - Update product (Admin)
- `DELETE /api/products/[id]` - Delete product (Admin)

### Categories, Users, Carts, etc.

- Similar CRUD endpoints for other entities

For detailed API documentation, refer to the code in `app/api/` directory.

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

### Development Guidelines

- Use TypeScript for all new code
- Follow the existing code style
- Write meaningful commit messages
- Test your changes thoroughly
- Update documentation as needed

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing framework
- [Shadcn/UI](https://ui.shadcn.com/) for beautiful UI components
- [TailwindCSS](https://tailwindcss.com/) for utility-first styling
- [MongoDB](https://www.mongodb.com/) for the database
- [Vercel](https://vercel.com/) for hosting and deployment

---

**Made with ❤️ by [tcuong2003](https://github.com/tcuong2003)**

If you find this project helpful, please give it a ⭐ on GitHub!
