<p align="center">
  <img width="180" height="180" src="/nodes/ApaleoAPI/apaleo.svg">
</p>


# n8n Nodes for Apaleo

This repository provides custom nodes for [n8n](https://n8n.io), enabling integration with Apaleo, a property management platform tailored for the hospitality industry. Use these nodes to automate workflows that interact with Apaleo's data and services.

To contribute and make this custom node available to the community, create it as an npm package and publish it to the npm registry.

## install

![Settings Animation](install.gif)

## Setup

### Get Apaleo API Credentials

1. Log in to your [Apaleo Developer account](https://developer.apaleo.com) to create and retrieve your API keys.

### Add Credentials to n8n

1. Go to **Settings** > **Credentials** in the n8n dashboard
2. Click **New** and select **Apaleo API**
3. Enter your Apaleo API credentials and save them

## Implemented Endpoints

The following Apaleo endpoints are currently supported:

### Booking

- **POST** `/booking/v1/bookings`  
  Creates a booking for one or more reservations.

- **GET** `/booking/v1/bookings`  
   Retrieve a list of bookings.

- **GET** `/booking/v1/bookings/{id}`  
  Retrieves a specific booking.

- **PATCH** `/booking/v1/bookings/{id}`  
  Allows modification of certain booking properties.

### Reservation

- **GET** `/booking/v1/reservations`  
  Returns a list of all reservations.

- **GET** `/booking/v1/reservations/{id}`  
  Retrieves a specific reservation.

- **PATCH** `/booking/v1/reservations/{id}`  
  Allows modification of certain reservation properties.

### Reservation Actions

- **PUT** `/booking/v1/reservation-actions/{id}/assign-unit`  
  Assign unit to reservation.

## Usage

After setting up the credentials, you can add Apaleo nodes to your workflows by selecting **Apaleo** in the node selection menu. Configure each node by choosing the relevant actions and fields provided by Apaleo.

### Example Use Case

**Automate Booking Management:**  
Create workflows that automatically retrieve and manage bookings, cancellations, and customer data from Apaleo. Integrate this data with other applications such as CRMs, email systems, and more.

## Development and Testing

### 1. Modify Example Nodes

Modify or replace the example nodes located in the `/nodes` and `/credentials` folders according to your needs.

### 2. Update `package.json`

Update the `package.json` file with your package details.

### 3. Lint the Code

Run the following command to check for errors:

```bash
npm run lint
```

To automatically fix errors, use:

```bash
npm run lintfix
```

### 4. Test Locally

Test your node locally to ensure everything works as expected. For more information, refer to the [documentation on running nodes locally](https://docs.n8n.io/nodes/creating-nodes/testing/).

## Support

If you encounter any issues or have feature requests, please open an issue in this repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
