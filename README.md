<br><h1 align="center">cashTrack:sparkles:</h1>

#### <p align="center">Split the bill without splitting the bill</p>
<br><br>


<p align="center"><img src="https://user-images.githubusercontent.com/105183376/229327292-d98418df-f291-45a6-b72a-5b6f663b2a24.gif" alt="cash track example"></p>
<br><br>

CashTrack is a powerful tool that helps you split bills without splitting them. It's easy to use and helps you keep track of your expenses with a friend or family member.

CashTrack is a bash script that allows two people to pay for each other for various bills such as groceries, rent, gas, etc. It leverages signal-cli to track who has been spending more and allows the other person to make up the difference by spending money on the next bill. The goal is to keep the difference spent between both individuals around 0 dollars. All transactions are stored in an SQL database and each user can use the Signal messenger application to *virtually* send and request money. This tool is intended to be used with a dedicated signal account.


## Installation
1. In a virtual machine, install signal-cli: https://github.com/AsamK/signal-cli
2. Create a new Signal account. (The phone number for this account will be the $USERNAME)
3. Install sqlite3: apt install sqlite3
4. Clone this repository: `git clone https://github.com/originates/cashTrack.git`


## Setup
1. start the signal-cli daemon using `signal-cli -u "$USERNAME" daemon &> "/dev/null" &`
2. Navigate to the cloned repository: `cd cashTrack`
3. Run `./cashTrack` to start the program.


## Usage

To use the program, users can use the following commands:
- `r ` for request
- `s ` for send
- `xx` to remove the last entry

CashTrack Example Usage:<br>
1.) Erica and Sam go to a coffee shop. Erica buys a coffee as well as a coffee and a donut for Sam.<br>
2.) Erica then sends the message `r 6.04 coffee and donut` to signal-bot since she wants to request that money from Sam.<br><br>
This will add 6.04 to Erica's balance and subtract 6.04 from Sam's balance.<br>
Both users will be notified instantly that the transaction succeeded and will tell them their new balance.<br>
The message will also include the note 'coffee and donut.'


## Reporting Bugs or Issues
If you find any bugs or issues with this project, please open an issue on GitHub.


## License
```
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
