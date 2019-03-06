# is-password-compromised

Check securely whether a password is listed on [haveibeenpwned.com](https://haveibeenpwned.com). The script was written to address the common concern of pasting your passwords into unknown web sited and quickly check a password status from the command prompt.

## Usage

Python 3 is required to run the script.

```sh
git clone https://github.com/yanivmo/is-password-compromised.git
cd is-password-compromised
./is-password-compromised 123456
```

The script prints the number of occurrences of the specified password in the database.

## Security

As you can see from this very short script, the password itself is never sent to the server. The password is hashed using SHA1 algorithm and only the first five digits (out of 40) are sent to the server as per the [haveibeenpwned API specification](https://haveibeenpwned.com/API/v2#SearchingPwnedPasswordsByRange).

Thanks to the great guys at [haveibeenpwned.com](https://haveibeenpwned.com) for the great service. This script is just a shortcut :)

