# Part 1 - Run the project locally as a Monolithic application

Now that you have set up the AWS PostgreSQL database and S3 bucket, and saved the environment variables, let's run the application locally.  It's recommended that you start the backend application first before starting the frontend application that depends on the backend API.

## Backend App

### Download Dependencies
Download all the package dependencies by running the following command from the `/project/udagram-api/` directory:
```bash
npm install .
```
### Run Locally
Run the application locally in a development environment. This has been configured so that the changes in your code take effect without needing to restart the server.
```bash
npm run dev
```

### Verification
Once this command is run successfully, visit the `http://localhost:8080/api/v0/feed` in your web browser to verify that the application is running. You should see a JSON payload.
![image](https://user-images.githubusercontent.com/68260816/176383818-16569c5a-d814-4cfd-81bc-aba3074b1a1b.png)


## Frontend App
### Download Dependencies
Download all the package dependencies by running the following command from the `/project/udagram-frontend/` directory:
```bash
npm install .
```

### Build and Run the Project
```bash
ionic build
ionic serve
```
#### This project requires the following node versions
![image](https://user-images.githubusercontent.com/68260816/175830243-11bdd564-c2d1-4329-8b28-65c3f2e59900.png)


> Note: If you don't have Ionic CLI installed already, revisit the prerequisites in the previous section for setup instructions.

### Verification
Visit `http://localhost:8100` in your web browser to verify that the application is running. You should see a web interface.
![image](https://user-images.githubusercontent.com/68260816/176398913-19245e47-6bb4-480d-8c2f-379dddb849a8.png)

Next, register and create a new post
![image](https://user-images.githubusercontent.com/68260816/181939212-b7cbb2e8-24a4-4d00-8938-cd2bed0a7db9.png)

your final snapshort should contain the uploaded image
![image](https://user-images.githubusercontent.com/68260816/181939935-46ad6db8-38f9-4afa-9b6e-a662c608a30b.png)

___

## Next Steps
At this point, you should have a fully working web application that interfaces with an API. Feel free to play around with the application and its code to get an idea of how it works.

The rest of this section will provide some optional steps for your code.

### Optional
#### Linting Code
It's useful to _lint_ your code so that changes in the codebase adhere to a coding standard. This helps alleviate issues when developers use different styles of coding.

`eslint` has been set up for TypeScript in the codebase for you. To lint your code, run the following:
```bash
npx eslint --ext .js,.ts src/
```
To have your code fixed automatically, run
```bash
npx eslint --ext .js,.ts src/ --fix
```
