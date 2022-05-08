# Week 4 Lab Report

> Due May 8, 2022 <br>
**Topic:** Lab 5 Challenges

---

## Streamlining `ssh` Configuration

* Normally when you call `ssh`, you also have to tell it your username, along with the server host. However, by streamlining this process, you'll be able to connect to server hosts without the need of typing your username.

* To do this, we first need to find our local ssh directory

    ![Image](Images/sshDirectory.png)

* Once you find it, you should see a `config` file.

    > If you don't have one, you can just create one

* Once you found it, open it up using any text editor. In my case, I will be using Notepad.

    ![Image](Images/openNotepad.png)

* After that, just type in the server host and your username in the following format:

    ```Java
    Host <host>
        HostName <host_name>
        User <username>
    ```

* As an example, this is what mine looks like:

    ![Image](Images/sshConfigNotepad.png)

* That's it. You're done.

* Now, when you want to connect to the server, you can just type `ssh <host>`, and it'll automatically connect you without requiring you to type your username like so:

    ![Image](Images/sshShortcut.png)

* Now that we've streamlined our ssh process, let's practice copying a file over to our server account by using `scp`

* As an example, I can run this command below to copy a file named `index.md` to my remote `ieng6` account

```powershell
    scp index.md ieng6:/home/linux/ieng6/cs15lsp22/cs15lsp22aea
```


&nbsp;
## Setup Github Access from ieng6

* Code Diff

&nbsp;
## Copy whole directories with `scp -r`

* 