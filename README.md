# Yoga Master 🧘‍♀️

A modern, responsive yoga and fitness website built with Next.js, featuring dynamic content management through Firebase and stunning parallax animations.

## ✨ Features

- **Dynamic Content Management**: Content powered by Firebase Firestore for easy updates
- **Smooth Animations**: Parallax scrolling effects and Framer Motion animations
- **Responsive Design**: Mobile-first approach ensuring great experience across all devices
- **Modern UI Components**:
  - Hero slider with engaging visuals
  - Benefits showcase section
  - Services overview
  - Customer testimonials
  - About section with parallax imagery
  - Contact form
- **Performance Optimized**: Built with Next.js for optimal performance and SEO
- **Analytics Integration**: Vercel Analytics for tracking user engagement

## 🚀 Tech Stack

- **Framework**: [Next.js 12](https://nextjs.org/)
- **UI Library**: [React 18](https://react.dev/)
- **Database**: [Firebase 9](https://firebase.google.com/)
- **Animations**: 
  - [Framer Motion](https://www.framer.com/motion/)
  - [React Scroll Parallax](https://react-scroll-parallax.damnthat.tv/)
- **Additional Libraries**:
  - React Player for video content
  - React Modal for interactive overlays
  - React CountUp for animated statistics
  - Swiper for touch-enabled sliders

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm or yarn
- A Firebase project with Firestore enabled

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/pixelxpr/yoga-master.git
   cd yoga-master
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure Firebase**
   
   Create a `.env` file in the root directory and add your Firebase configuration:
   ```env
   NEXT_PUBLIC_FIREBASE_API_KEY=your_api_key
   NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
   NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
   NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
   NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
   NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
   
   # For Firebase Admin (optional)
   FIREBASE_CLIENT_EMAIL=your_client_email
   FIREBASE_PRIVATE_KEY=your_private_key
   ```

4. **Set up Firestore Collections**
   
   Create the following collections in your Firebase Firestore with the exact field names specified below. Each collection should have at least one document (the app reads the first document `[0]`).

   ### Collection: `Slider`
   Fields for the hero slider:
   - `slideDelay` (number) - Delay between slides in milliseconds
   - `img1_url` (string) - URL for first slide image
   - `img1_text` (string) - Text overlay for first slide
   - `img2_url` (string) - URL for second slide image
   - `img2_text` (string) - Text overlay for second slide
   - `img3_url` (string) - URL for third slide image
   - `img3_text` (string) - Text overlay for third slide

   ### Collection: `Benefits of Yoga`
   Fields for the benefits section:
   - `Title` (string) - Main section title
   - `image` (string) - Background image URL
   - `Title1` to `Title12` (string) - Individual benefit titles
   - `Body1` to `Body12` (string) - Individual benefit descriptions

   ### Collection: `Our Services`
   Fields for the services section:
   - `Title` (string) - Main section title
   - `Tile1` to `Tile6` (string) - Service descriptions
   - `image1` to `image6` (string) - Service thumbnail images
   - `video1` to `video6` (string) - Service video URLs

   ### Collection: `Happy Customers`
   Fields for statistics/testimonials:
   - `section1 title` (string) - First statistic label
   - `section1 body` (number) - First statistic value
   - `section2 title` (string) - Second statistic label
   - `section2 body` (number) - Second statistic value
   - `section3 title` (string) - Third statistic label
   - `section3 body` (number) - Third statistic value

   ### Collection: `About`
   Fields for the about section:
   - `Title` (string) - Section title
   - `Body` (string) - First paragraph
   - `Body1` (string) - Second paragraph
   - `Body2` (string) - Third paragraph
   - `image` (string) - Background image URL

   ### Collection: `Contact us`
   Fields for the contact section:
   - `Title` (string) - Section title
   - `Body` (string) - Description text
   - `Sub-Title` (string) - Subsection title
   - `Contact_text` (string) - Contact information text
   - `Phone` (string) - Phone number (without +91)
   - `Email` (string) - Email address
   - `image` (string) - Background image URL
   - `insta` (string) - Instagram profile URL
   - `yt` (string) - YouTube channel URL
   - `fb` (string) - Facebook page URL

## 🎯 Usage

### Development Mode

Run the development server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

### Production Build

Build the application for production:
```bash
npm run build
```

Start the production server:
```bash
npm start
```

### Deploy to Firebase

The project includes Firebase hosting configuration. Deploy with:
```bash
firebase deploy
```

## 📁 Project Structure

```
yoga-master/
├── components/          # React components
│   ├── About.js        # About section
│   ├── Benefits.js     # Benefits showcase
│   ├── Contact.js      # Contact form
│   ├── Footer.js       # Footer component
│   ├── Header.js       # Header component
│   ├── HappyCustomers.js # Testimonials
│   ├── Nav.js          # Navigation
│   ├── OurServices.js  # Services section
│   ├── Slider.js       # Hero slider
│   └── ...
├── pages/              # Next.js pages
│   ├── _app.js        # App wrapper
│   ├── _document.js   # Document structure
│   └── index.js       # Home page
├── styles/            # CSS modules
├── firebase/          # Firebase configuration
├── public/            # Static assets
├── .env               # Environment variables
└── package.json       # Dependencies
```

## 🎨 Customization

### Updating Content

Content is managed through Firebase Firestore. Update your collections to change:
- About section text and images
- Service offerings
- Customer testimonials
- Benefits information

### Styling

Styles are organized in CSS modules within the `styles/` directory. Each component has its corresponding CSS module for scoped styling.

## 🔧 Configuration

### Firebase Setup

1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database
3. Copy your configuration to `.env`
4. Set up Firestore security rules as needed

### Gitpod Support

The project includes `.gitpod.yml` for cloud-based development environments.

## 📦 Build & Export

To create a static export:
```bash
npm run build
```

This will generate an optimized production build and export static files to the `out/` directory.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is private and proprietary.

## 🙏 Acknowledgments

- Built with ❤️ using Next.js and React
- Powered by Firebase
- Animations by Framer Motion and React Scroll Parallax

## 📞 Support

For support or questions, please use the contact form on the website or reach out through the repository issues.

---

**Made with 🧘‍♀️ by Shape up with Ana**
