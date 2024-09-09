```markdown
# Device Down Detector

## Description

This repository contains two projects that detect if a device is down by retrieving the IP addresses of the downed devices from a SQL database. The first project is a **Spring Boot application**, and the second is an **Azure Functions** project.

## How to Run

### Spring Boot Project

Follow these steps to run the Spring Boot project:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/maheladissa/DeviceDownDetectorSpring.git
   ```

2. **Navigate to the Spring Boot project directory:**

   ```bash
   cd DeviceDownDetectorSpring
   ```

3. **Build the project:**

   ```bash
   mvn clean install
   ```

4. **Run the Spring Boot application:**

   ```bash
   mvn spring-boot:run
   ```

### Azure Functions Project

Follow these steps to run the Azure Functions project:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/maheladissa/DeviceDownDetector.git
   ```

2. **Navigate to the Azure Functions project directory:**

   ```bash
   cd DeviceDownDetector
   ```

3. **Package the project:**

   ```bash
   mvn package
   ```

4. **Run the Azure Functions locally:**

   ```bash
   mvn azurefunctions:run
   ```

## How to Test via Postman

### Spring Boot Project

#### Test Locally

1. **Open Postman.**

2. **Create a new request:**

    - Set the request method to `GET`.
    - Use the following URL:

      ```
      http://localhost:<port>/api/devices/down
      ```

    - Replace `<port>` with the actual port number your Spring Boot application is running on.

3. **Send the request:**

    - Click `Send` to test the API endpoint.

4. **Review the response:**

    - Check the response status code, body, and headers to ensure the API is functioning as expected.

#### Test Cloud

1. **Open Postman.**

2. **Create a new request:**

    - Set the request method to `GET`.
    - Use the following URL:

      ```
      https://downdetectorspring.test.azuremicroservices.io/downdetector-184756/default/api/devices/down
      ```

3. **Set up Basic Auth:**

    - In the `Authorization` tab, select `Basic Auth`.
    - Enter your Azure app credentials (username and password).

4. **Send the request:**

    - Click `Send` to test the API endpoint.

5. **Review the response:**

    - Check the response status code, body, and headers to ensure the API is functioning as expected.

### Azure Functions Project

#### Test Locally

1. **Open Postman.**

2. **Create a new request:**

    - Set the request method to `GET`.
    - Use the following URL:

      ```
      http://localhost:7071/api/GetDownIPAddresses?
      ```

3. **Send the request:**

    - Click `Send` to test the API endpoint.

4. **Review the response:**

    - Check the response status code, body, and headers to ensure the API is functioning as expected.

#### Test Cloud Demo

1. **Open Postman.**

2. **Create a new request:**

    - Set the request method to `GET`.
    - Use the following URL:

      ```
      https://iotservices-18293.azurewebsites.net/api/GetDownIPAddresses?
      ```

3. **Add Authentication headers:**

    - In the `Headers` tab, add the following key-value pair:

      ```
      x-functions-key: <Your Function Key>
      ```

4. **Send the request:**

    - Click `Send` to test the API endpoint.

5. **Review the response:**

    - Check the response status code, body, and headers to ensure the API is functioning as expected.
```