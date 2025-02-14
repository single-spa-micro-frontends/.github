# Single-SPA Micro Frontend

This organization contains a micro frontend architecture for an e-commerce platform focused on selling books. The project uses React, Vite, and Single-SPA(vite) to create independently deployable applications.

## Features
- **Root Config (Single-SPA, Vite):**
  - The entry point of the application is where all micro frontends are injected.
  - Manages layout and routing of the micro frontends.
  - Imports and integrates all micro frontends.

- **Header (React):**
  - Provides a header component with search and cart UI.
  - Dispatches and consumes the events from the Event Bus.
 
- **Footer (React):**
  - Provides a footer component with different book categories for filtering.
  - Dispatches and consumes the events from the Event Bus.
  
- **Books List App (React):**
  - Fetches and displays a list of programming books.
  - Allows users to select a book to view more details or add to a cart.
  - Dispatches and consumes the events from the Event Bus.

- **Single Book App (React):**
  - Displays details of a selected book.
  - Allows users to add the book/books to the cart.
  - Dispatches and consumes the events from the Event Bus.
 
- **Event Bus (Vite, RxJS):**
  - State-holding micro frontend providing subscribable objects and events/
  - Used as the main channel of communication between micro frontends.

## 🚀 Technologies Used

- **React** - Frontend framework for all micro frontends.
- **Vite** - Build tool for fast development and optimized production builds.
- **Single-SPA** - Enables independent deployment and dynamic imports of micro frontends.
- **RxJS** - Used for global state management across micro frontends.

## 🛠 Installation & Setup

### Clone the repositories:
```sh
git clone git@github.com:single-spa-micro-frontends/root-config.git
git clone git@github.com:single-spa-micro-frontends/header.git
git clone git@github.com:single-spa-micro-frontends/footer.git
git clone git@github.com:single-spa-micro-frontends/book-list.git
git clone git@github.com:single-spa-micro-frontends/single-book.git
git clone git@github.com:single-spa-micro-frontends/event-bus.git
```

### Install dependencies for each repository:
```sh
pnpm install 
```

### Run each application:
```sh
pnpm run dev
```

Each application will have a white screen, and you won't be able to see the UI for single mf, the applications will be visible only on port 3005 since that is root-config, main entry point of the aplicaiton.

## 🤝 Contribution
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Add feature"`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

## 📜 License

This project is licensed under the [MIT License](LICENSE).

