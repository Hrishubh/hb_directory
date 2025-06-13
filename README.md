
# <a name="introduction">HB Directory - Startup Pitch Platform</a>

A modern web application that serves as a comprehensive directory for budding startups, allowing entrepreneurs to showcase their ideas, connect with like-minded individuals, and participate in virtual pitch competitions.


## <a name="tech-stack">⚙️ Tech Stack</a>

- **Frontend** : Next.js 15 (React 19 RC), TypeScript
- **Styling** : Tailwind CSS, Radix UI components
- **Authentication** : NextAuth.js with GitHub provider
- **Database** : Sanity CMS
- **Deployment** : Vercel-ready configuration
- **Monitoring** : Sentry integration for error tracking
- **UI Components** : Custom components with shadcn/ui


## <a name="tech-stack">📋 Prerequisites</a>

Before setting up the project, ensure you have:

- Node.js 18+ installed
- npm or yarn package manager
- GitHub account for authentication
- Sanity account for content management

## <a name="features">🔋 Features</a>

👉 **Live Content API**: Displays the latest startup ideas dynamically on the homepage using Sanity's Content API.

👉 **GitHub Authentication**: Allows users to log in easily using their GitHub account.

👉 **Pitch Submission**: Users can submit startup ideas, including title, description, category, and multimedia links (
image or video).

👉 **View Pitches**: Browse through submitted ideas with filtering options by category.

👉 **Pitch Details Page**: Click on any pitch to view its details, with multimedia and description displayed.

👉 **Profile Page**: Users can view the list of pitches they've submitted.

👉 **Editor Picks**: Admins can highlight top startup ideas using the "Editor Picks" feature managed via Sanity Studio.

👉 **Views Counter**: Tracks the number of views for each pitch instead of an upvote system.

👉 **Search**: Search functionality to load and view pitches efficiently.

👉 **Minimalistic Design**: Fresh and simple UI with only the essential pages for ease of use and a clean aesthetic.

and many more, including the latest **React 19**, **Next.js 15** and **Sanity** features alongside code architecture and
reusability.

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

**Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

**Cloning the Repository**

```bash
git clone <your-repository-url> #This repository or clone repository
cd hb_directory
```

**Installation**

Install the project dependencies using npm:

```bash
npm install
```

**Set Up Environment Variables**

Create a new file named `.env.local` in the root of your project and add the following content:

```env
NEXT_PUBLIC_SANITY_PROJECT_ID=
NEXT_PUBLIC_SANITY_DATASET=
NEXT_PUBLIC_SANITY_API_VERSION='vX'
SANITY_TOKEN=

AUTH_SECRET= 
AUTH_GITHUB_ID=
AUTH_GITHUB_SECRET=
```

Replace the placeholder values with your actual Sanity credentials. You can obtain these credentials by signing up & creating a new project on the [Sanity website](https://www.sanity.io/).

- `NEXT_PUBLIC_SANITY_PROJECT_ID` and `NEXT_PUBLIC_SANITY_DATASET`: These can be found in your Sanity project dashboard.
-   `SANITY_API_WRITE_TOKEN`: Generate this token in your Sanity project settings under "API" -> "Tokens". Ensure it has write permissions.
-   `GITHUB_ID` and`GITHUB_SECRET`: Obtain these by setting up a new OAuth App on GitHub (see next step).
-   `NEXTAUTH_SECRET`: A random string used to encrypt NextAuthjs sessions. You can generate one using `openssl rand -base6432` in your terminal.
-   `NEXTAUTH_URL`: The URL of your application. For local development, it's `http:/localhost:3000`.

**Sanity Setup**:

-   Go to [Sanity.io](https:/www.sanity.io/) and create anew project.
-   Replace the placeholdervalues in `.env.local` withyour actual Sanity credentials.You can obtain thesecredentials by signing up &creating a new project on the[Sanity website](https://wwwsanity.io/).
-   Deploy your Sanity schema:Navigate to the `sanity`directory and run:

    ```bash
    cd sanity
    npx sanity deploy
    ```

    Follow the prompts todeploy your studio. This will make your schema typesavailable in your Sanityproject.

**GitHub OAuth App Setup**:

-   Go to your GitHub settings -> Developer settings -> OAuth Apps -> New OAuth App.
-   **Application name**: Choose a name for your app (e g., "Startup Directory Dev").
-   **Homepage URL**: `http:/ localhost:3000`
-   **Authorization callback URL**: `http://localhost:3000/api/auth/callback/github`
-   After creating the app, you will get your `Client ID` (GITHUB_ID) and `Client Secret` (GITHUB_SECRET).

**Running the Project**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the project.

## <a name="links">🔗 Assets</a>

- Fonts and Assets used in the project can be found [here](https://drive.google.com/file/d/1OEFHnEq5pQFP86u8FOBLBBNxKPsbjjqU/view?usp=sharing)
- [Learn Server Actions](https://youtu.be/FKZAXFjxlJI?feature=shared)
- [Applicaton Workflow](https://miro.com/app/board/uXjVLT_tMdU=/?share_link_id=580854757703)


## <a name="more">🚀 More</a>

**Based on Youtube Tutorial**

This project is based on a tutorial video. If you're interested in building something similar or learning more about the technologies used, you can find the tutorial here: <u>[**Link to YouTube Tutorial**](https://www.youtube.com/watch?v=Zq5fmkH0T78)</u>