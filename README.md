## Building the Docker Image

To build the Docker image for the React frontend application, navigate to the directory containing the Dockerfile and run:

```bash
docker build -t react-frontend .
```

## Running the Docker Container

Run the Docker container with the following command:

```bash
docker run -p 80:80 react-frontend
```

Access the application at [http://localhost](http://localhost).

## Additional Information

For further customization, such as using environment variables or adding additional configurations, refer to the [Docker documentation](https://docs.docker.com/).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- Thanks to Docker for providing a robust containerization solution.
- Node.js and React teams for their fantastic tools.

---

This README provides clear instructions for building and running Docker containers for both the Node.js backend and the React frontend applications. Feel free to modify this to include additional pro
