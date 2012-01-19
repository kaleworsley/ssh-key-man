# ssh-key-man


Manage and distribute public keys.

## Commands

    add-key [user] [name] [key] | [key file]  # Adds a public key to a users list of keys in ~/.ssh/public_keys

    authorize [user] [target]                 # Adds the users keys to the target users authorized_keys

    deauthorize [user] [target]               # Removes the users keys from the target users authorized_keys

    list-keys [user]                          # List a users public keys

## Example Usage

Add Bob's work public key to ~/.ssh/public_keys

    bob@workpc $ ssh-key-man add-key bob workpc ~/.ssh/id_rsa.pub


Add Bob's laptop public key to ~/.ssh/public_keys

    bob@workpc $ ssh-key-man add-key bob laptop "ssh-rsa ..."

Authorize Bob to access Steve's account

    bob@workpc $ sudo ssh-key-man authorize bob steve




## License
Copyright (C) 2012 Kale Worsley kale@egressive.com

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see http://www.gnu.org/licenses/.


