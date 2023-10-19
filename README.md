# CloudMirror: Seamless End-to-End Encryption for Cloud Storage and Sharing
A secure cloud file storage and sharing tool, put a lock on your shared cloud files.


## Install
- Install your cloud clients.

Some of the tested cloud clients are as follows.

|  Name   | URL  |
|  ----  | ----  |
| Dropbox           | [https://www.dropbox.com](https://www.dropbox.com/install) |
| OneDrive          | [https://www.microsoft.com/en-us/microsoft-365/onedrive](https://www.microsoft.com/en-us/microsoft-365/onedrive/download) |
| Google Drive      | [https://www.google.com/intl/en-GB/drive](https://www.google.com/intl/en-GB/drive/download/) |
| iCloud            | [https://www.icloud.com/iclouddrive](https://support.apple.com/en-gb/HT204283) |
| Yandex            | [https://disk.yandex.com](https://disk.yandex.com/promo/download) |
| Nutstore          | [https://www.jianguoyun.com/](https://www.jianguoyun.com/s/downloads) |
| CloudMe           | [https://www.cloudme.com](https://www.cloudme.com/zh/sync) |
| Mega              | [https://mega.io](https://mega.io/desktop) |
| NextCloud         | [https://nextcloud.com](https://nextcloud.com/install/) |
| ownCloud          | [https://owncloud.com](https://owncloud.com/desktop-app/) |
| Syncthing         | [https://syncthing.net](https://syncthing.net/downloads/) |
| Seafile           | [https://www.seafile.com](https://www.seafile.com/en/download/) |
| Kodbox            | [https://github.com/kalcaddle/kodbox](https://github.com/kalcaddle/kodbox/releases) |

- Install the fuse file system

- [x] Windows: 
WinFsp: <https://winfsp.dev/rel/>
  - Download and run the WinFsp installer.
- [ ] MacOS, Temporarily unavailable.
- [ ] Linux, Temporarily unavailable.


## Usage
As an example, let's consider how to use CloudMirror with Dropbox.

- **Step 1.** Generate your RSA key pairs

```bash
# Generate RSA private key
$ openssl genrsa -out AliceSK.pem 4096

# Generate RSA public key
$ openssl rsa -in AliceSK.pem -pubout -out AlicePK.pem
```

- **Step 2.** Login to CloudMirror 

    - Key path: Enter the path of your private key.
    - Policy path: Enter the path of the sharing policy file (i.e., the root path of your cloud drive).
    - Mount point: Enter the disk letter for mounting. (Z: by default).

![](/images/login.png)

- **Step 3.** Add your friends' public keys.
    - Click the `User Management` tab, enter the corresponding public key of your shared friends in Dropbox.

 ![](/images/user.png)

 - **Step 4.** Set your sharing policy.
    - Set your sharing policy in the `Sharing Management` tab.

![](/images/sharing.png)

- **[Optional]** Multiple clouds management.
    - Enter multiple cloud paths here if you need to manage multiple clouds at the same time.

![](/images/multidisk.png)


- **Step 5.** Share your cloud folders
    - Share your cloud folders with your friends in Dropbox.
    - Write a file in the cloud sync folder where the sharing policy is set. (*The result before and after encryption is shown in the following figure.*)
    - Now, enjoy the secure file sharing.

![](/images/encryption.png)


## License
This project is dual-licensed under the GPLv3 for FOSS projects as well as a commercial license for independent software vendors and resellers. If you want to modify this application under different conditions, feel free to contact our support team.