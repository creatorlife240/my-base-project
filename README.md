// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Guestbook {
    struct Entry {
        address sender;
        string name;
        string message;
        uint256 timestamp;
    }

    Entry[] public entries;

    event NewEntry(address indexed sender, string name, string message);

    // Function to sign the guestbook
    function signGuestbook(string memory _name, string memory _message) public {
        entries.push(Entry(msg.sender, _name, _message, block.timestamp));
        emit NewEntry(msg.sender, _name, _message);
    }

    // Function to get all entries
    function getAllEntries() public view returns (Entry[] memory) {
        return entries;
    }
}
