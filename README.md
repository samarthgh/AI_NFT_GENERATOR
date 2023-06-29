# AI NFT Generator

This is a project that generates images using the Stable Diffusion API and mints them as NFTs by making transactions using MetaMask and putting the NFTs on the blockchain.

## Technologies Used

- React
- Hugging Face API (Stable Diffusion 2 Model)
- NFT.Storage
- ethers.js
- axios
- MetaMask

## Getting Started

To run the project locally, follow these steps:

1. Clone the repository: `git clone <repository-url>`
2. Navigate to the project directory: `cd <project-directory>`
3. Install the dependencies: `npm install`
4. Start the development server: `npm start`
5. Open your browser and visit: `http://localhost:3000`

Note: Make sure you have MetaMask installed and configured in your browser.

## Project Structure

The project structure is as follows:

- `components`: Contains the reusable components used in the project.
- `abis`: Contains the ABIs (Application Binary Interfaces) for the smart contracts.
- `config.json`: Configuration file containing network-specific information.
- `App.js`: Main component that contains the logic for generating and minting NFTs.
- `index.js`: Entry point of the React application.

## How It Works

1. The application loads the blockchain data and connects to the Ethereum network using MetaMask.
2. The user enters a name and description for the NFT.
3. On form submission, the application generates an image using the Stable Diffusion API.
4. The generated image is uploaded to IPFS using the NFT.Storage service.
5. The metadata for the NFT is obtained from IPFS.
6. The NFT is minted by calling the `mint` function on the smart contract, passing the tokenURI and the required value in Ether.
7. The transaction is confirmed, and the NFT is minted on the blockchain.
8. The user can view the generated image and the metadata of the NFT.

## Screenshots

1. User enters name and description of the required image.

<img width="1440" alt="Screenshot 2023-06-29 at 11 00 11 PM" src="https://github.com/samarthgh/AI_NFT_GENERATOR/assets/94733648/7aa207c2-4b2a-4762-b5f6-1f3f31e37f9a">

2. Spinner prompts the user to wait while the request is being sent.
   
<img width="1440" alt="Screenshot 2023-06-29 at 11 00 26 PM" src="https://github.com/samarthgh/AI_NFT_GENERATOR/assets/94733648/1238ad78-15fb-45fa-9dae-60c9f7599e0a">

3. Metamask ask the user to approve the transaction.
   
<img width="1440" alt="Screenshot 2023-06-29 at 11 00 42 PM" src="https://github.com/samarthgh/AI_NFT_GENERATOR/assets/94733648/dbde565e-9bad-4e4e-b284-addb440cca2b">

4. Final image is displayed after the transaction.

<img width="1438" alt="Screenshot 2023-06-29 at 11 02 55 PM" src="https://github.com/samarthgh/AI_NFT_GENERATOR/assets/94733648/bd3bd653-194e-4c7c-a9a8-776c16697567">




## Dependencies

- `react-bootstrap`: For styling and components.
- `nft.storage`: JavaScript library for interacting with the NFT.Storage service.
- `ethers`: Ethereum library for interacting with smart contracts.
- `axios`: HTTP client for making API requests.

## Environment Variables

The project relies on the following environment variables:

- `REACT_APP_HUGGING_FACE_API_KEY`: API key for the Stable Diffusion API.
- `REACT_APP_NFT_STORAGE_API_KEY`: API key for the NFT.Storage service.

Make sure to set these environment variables before running the project.

## License

This project is licensed under the [MIT License](LICENSE).
