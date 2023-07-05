# email-signature

<img src="email-signature.png">
<img src="email-signature-dark.png">

## How to choose your signature ?

### Gmail signature
* Gmail signature works on all mailbox
* Doesn't change with the theme
* Designed to be used on a white background
* Need internet connexion

### Mac signature
* Works on svg compatible mailbox, check <a href="https://css-tricks.com/a-guide-on-svg-support-in-email/">here</a> for compatibility
* Adapt with the theme (only checked on Mail with Ventura)
* High quality images
* Doesn't need internet connexion

## How to use it on Gmail ?

1. Open signature.html file on your browser
2. * Windows / Linux: Use Ctr + A, Ctr + C
   * MacOS: Use ⌘ + A, ⌘ + C
3. Go to your gmail account and open parameters
4. In the Signature section, create a new one
5. * Windows / Linux: Use Ctr + v
   * MacOS: Use ⌘ + V
6. Save changes

## How to use it on Mail (MacOs) ?

1. Create a blank signature, tutorial <a href="https://support.apple.com/en-ie/guide/mail/mail11943/mac">here</a>.
2. Quit and Close Mail.
3. Open System Settings, click Privacy & Security, then click Full Disk Access and add Terminal application
4. Open a terminal and enter the following command:
    ```shell
    cd ~/Library/Mail/V{version number}/MailData/Signatures
    ```
5. Find the filename with .mailsignature extension of your signature based on the creation date:
    ```shell
    ls -sl
    ```
6. Open the file using a text editor and replace the body content with the content of signature.html
7. Quick way using vim:
    * Open the file
        ```shell
        vim {filename}.mailsignature
        ```
    * Delete the body line (double press d)
    * Press i to pass in insert mode
    * Write a body balise and paste the html code.
    * Press esc, :wq, ↩ to save and close the file

8. On the Terminal enter the following command to lock your signature file:
    ```shell
    chflags uchg {file_name}.mailsignature
    ```
9. Open Mail and try your new signature !
10. For security reason, remove Full Disk Access to the Terminal application

Another tutorial using MacOs UI <a ref="https://www.hubspot.com/email-signature-generator/add-html-signature-mail-mac">

## Et voilà !