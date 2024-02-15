# E-Commerce Full Stack + Dashboard

Next.js 13, App Router, React, Tailwind, Prisma, MySQL

# Installation

### Cloning the repository

```shell

git clone https://github.com/AntonioErdeljac/next13-ecommerce-admin.git
```

### Install packages

```shell

npm i
```

### Setup .env file

```js
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/
DATABASE_URL=''
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=""
STRIPE_API_KEY=
FRONTEND_STORE_URL=http://localhost:3001
STRIPE_WEBHOOK_SECRET=
```

### Connect to PlanetScale

```shell

npx prisma generate
```

### Push Prisma

```shell

npx prisma db push
```

### Start the app

```shell

npm run dev
```

### Go to [Coudinary](https://cloudinary.com/) and get Cloud Name

### E-Commerce Admin > components > ui > image-upload.tsx [Line - 56]

```tsx
<CldUploadWidget onUpload={onUpload} uploadPreset="CLOUD_NAME">
```

### Go to app - Billboards - Add New - ... - Copy Id

### E-Commerce Store > app > (routes) > page.tsx [Line - 11]

```tsx
const billboard = await getBillboard("CHANGE_ME_WITH_ID");
```

[Stripe Testing Cards](https://stripe.com/docs/testing)

[VIDEO TUTORIAL](https://youtu.be/5miHyP6lExg)

Key Features:

- We will be using Shadcn UI for the Admin!
- Our admin dashboard is going to serve as both CMS, Admin and API!
- You will be able to control mulitple vendors / stores through this single CMS! (For example you can have a "Shoe store" and a "Laptop store" and a "Suit store", and our CMS will generate API routes for all of those individually!)
- You will be able to create, update and delete categories!
- You will be able to create, update and delete products!
- You will be able to upload multiple images for products, and change them whenever you want!
- You will be able to create, update and delete filters such as "Color" and "Size", and then match them in the "Product" creation form.
- You will be able to create, update and delete "Billboards" which are these big texts on top of the page. You will be able to attach them to a single category, or use them standalone (Our Admin generates API for all of those cases!)
- You will be able to Search through all categories, products, sizes, colors, billboards with included pagination!
- You will be able to control which products are "featured" so they show on the homepage!
- You will be able to see your orders, sales, etc.
- You will be able to see graphs of your revenue etc.
- You will learn Clerk Authentication!
- Order creation
- Stripe checkout
- Stripe webhooks
- MySQL + Prisma + PlanetScale
