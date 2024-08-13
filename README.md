Method 1 : MULTI STAGE BUILD

![Screenshot 2024-08-01 114042](https://github.com/user-attachments/assets/fbac2550-870a-4d01-902e-544542d97974)


Method 2  : DOCKER LAYER
Reference : https://docs.docker.com/build/guide/layers/

![image](https://github.com/user-attachments/assets/74395b64-1076-41c2-a3f1-072317486f02)


Method 3  : SCRATCH IMAGE
Reference : https://hub.docker.com/_/scratch/

![image](https://github.com/user-attachments/assets/91d3fecd-2281-453f-ad1d-14d2341e4adc)

## Dockerfile Explanation

The multistage Dockerfile consists of two build stages, each optimized for a specific purpose.

### Stage 1: Build the Flask Application

- Use a Python base image to build the Flask backend.
- Copy the backend source code and install dependencies.
- Build the Flask application.

### Stage 2: Final Image

- Use a minimal Python base image for the final image.
- Copy the built backend from Stage 1.
- Expose the necessary port and start the Flask application.

