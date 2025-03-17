# Blockchain for Car Rentals

## Project Title: Blockchain for Car Rentals

## Project Vision:
The vision of this project is to create a decentralized and transparent car rental system that eliminates the need for intermediaries. By leveraging blockchain technology, users can securely rent and lend vehicles with trust and ease.


## Project Description
This smart contract establishes a decentralized, peer-to-peer car rental ecosystem, empowering individuals to lease their vehicles without the need for intermediaries. By leveraging blockchain technology, the platform ensures unparalleled transparency, security, and automation in rental transactions.

## Features
- **Seamless Car Listing**: Owners can effortlessly register their vehicles, specifying model details and daily rental pricing.
- **Efficient Car Rental Process**: Renters can easily book available cars by making secure payments in Ether.
- **Automated Payment System**: Funds are directly transferred to the car owner's wallet upon successful rental.
- **Rental Completion Mechanism**: Renters can officially conclude the rental period, making the car available for future users.
- **Dynamic Project Information Management**: The contract owner holds the authority to update the project title and description.

## Contract Address
0x98751ccc48a27d70996fd992120e4c2fa95e723f

## Smart Contract Functions
### 1. `listCar(string memory _model, uint256 _pricePerDay) public`
- Enables car owners to register their vehicle for rental.
- Triggers the `CarListed` event upon successful listing.

### 2. `rentCar(uint _carId, uint256 _rentalDays) public payable`
- Allows users to rent a car for a specified duration.
- Transfers rental fees directly to the owner’s account.
- Emits the `CarRented` event.

### 3. `completeRental(uint _rentalId) public`
- Grants renters the ability to finalize their rental period.
- Restores the vehicle’s availability for subsequent rentals.
- Triggers the `RentalCompleted` event.

### 4. `getProjectDetails() public view returns (string memory, string memory)`
- Retrieves and displays the project title and description.

### 5. `updateProjectDetails(string memory _title, string memory _description) public onlyOwner`
- Authorizes the contract owner to modify the project’s title and description.

## Events
- `CarListed(uint carId, string model, uint256 pricePerDay, address owner)` – Logs newly listed cars.
- `CarRented(uint carId, address renter, uint256 rentalStart, uint256 rentalEnd)` – Captures rental transactions.
- `RentalCompleted(uint carId, address renter)` – Confirms rental completion and car availability restoration.

## License
This project is released under the MIT License.


## Future Scope:
- Integration with IoT devices for automated access control.
- Smart contract-based insurance policies.
- Expansion to a global peer-to-peer car rental market.
- Incorporation of decentralized identity verification.



