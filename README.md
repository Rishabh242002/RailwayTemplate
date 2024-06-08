# PrestaShop Docker Template with PostgreSQL

This template sets up a PrestaShop environment using Docker and Docker Compose with PostgreSQL, ready for deployment on Railway.

## Prerequisites

- Docker
- Docker Compose
- Railway CLI (optional, for local development)

## Setup

1. Clone the repository:
    ```sh
    git clone <repository-url>
    cd prestashop-docker
    ```

2. Copy the `.env.example` to `.env` and update the variables as needed:
    ```sh
    cp .env.example .env
    ```

3. Start the containers locally (optional):
    ```sh
    docker-compose up -d
    ```

4. Deploy to Railway:
    - Sign up or log in to [Railway](https://railway.app)
    - Create a new project
    - Follow the instructions to deploy using the Railway GitHub integration

## Cleanup

To stop and remove the containers and their volumes locally, run:
```sh
docker-compose down -v

#### Step 5: Deploy to Railway

1. **Sign Up/Log In**: Go to [Railway](https://railway.app) and sign up or log in.
2. **Create a New Project**: Click on "New Project" and follow the steps to create a new project.
3. **Link GitHub Repository**: Connect your GitHub account and link the repository containing your `docker-compose.yml` and `.env.example` files.
4. **Set Environment Variables**: Go to the "Variables" section in the Railway dashboard and set the necessary environment variables based on your `.env.example` file.

   For example:
   - `PS_INSTALL_AUTO=1`
   - `PS_ERASE_DB=1`
   - `PS_DEV_MODE=false`
   - `PS_HOST_MODE=false`
   - `ADMIN_MAIL=admin@example.com`
   - `ADMIN_PASSWD=admin123`
   - `PS_LANGUAGE=en`
   - `PS_COUNTRY=US`
   - `PS_TIMEZONE=America/New_York`
   - `PS_DOMAIN=your-railway-app-domain`
   - `DB_HOST=db`
   - `DB_NAME=prestashop`
   - `DB_USER=prestashop`
   - `DB_PASSWORD=prestashop`

5. **Deploy**: After setting the environment variables, deploy the project. Railway will handle the rest and spin up your containers based on the `docker-compose.yml`.

#### Step 6: Access PrestaShop

Once the deployment is complete, you can access PrestaShop via the Railway-provided domain:

- **Storefront**: `http://your-railway-app-domain`
- **Admin Panel**: `http://your-railway-app-domain/admin`

Use the admin email and password specified in your environment variables to log in.

### Conclusion

By organizing your project directory, using a `.env.example` file, documenting the setup in a `README.md`, and deploying via Railway, you create a reusable and deployable Docker Compose template for PrestaShop with PostgreSQL. This setup makes it easy to deploy and manage PrestaShop on the Railway platform.
