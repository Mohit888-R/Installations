# Linux : 

### Install Rust for the Current User
``` curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh ```

```
Output
sammy@ubuntu:~$ curl --proto '=https' --tlsv1.3 https://sh.rustup.rs -sSf | sh
info: downloading installer

Welcome to Rust!

This will download and install the official compiler for the Rust
programming language, and its package manager, Cargo.

Rustup metadata and toolchains will be installed into the Rustup
home directory, located at:

  /home/sammy/.rustup

This can be modified with the RUSTUP_HOME environment variable.

The Cargo home directory is located at:

  /home/sammy/.cargo

This can be modified with the CARGO_HOME environment variable.

The cargo, rustc, rustup and other commands will be added to
Cargo's bin directory, located at:

  /home/sammy/.cargo/bin

This path will then be added to your PATH environment variable by
modifying the profile files located at:

  /home/sammy/.profile
  /home/sammy/.bashrc

You can uninstall at any time with rustup self uninstall and
these changes will be reverted.

Current installation options:


   default host triple: x86_64-unknown-linux-gnu
     default toolchain: stable (default)
               profile: default
  modify PATH variable: yes

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
>1

info: profile set to 'default'
info: default host triple is x86_64-unknown-linux-gnu
info: syncing channel updates for 'stable-x86_64-unknown-linux-gnu'
info: latest update on 2023-01-10, rust version 1.66.1 (90743e729 2023-01-10)
info: downloading component 'cargo'
info: downloading component 'clippy'
info: downloading component 'rust-docs'
info: downloading component 'rust-std'
info: downloading component 'rustc'
 67.4 MiB /  67.4 MiB (100 %)  40.9 MiB/s in  1s ETA:  0s
info: downloading component 'rustfmt'
info: installing component 'cargo'
  6.6 MiB /   6.6 MiB (100 %)   5.5 MiB/s in  1s ETA:  0s
info: installing component 'clippy'
info: installing component 'rust-docs'
 19.1 MiB /  19.1 MiB (100 %)   2.4 MiB/s in  7s ETA:  0s
info: installing component 'rust-std'
 30.0 MiB /  30.0 MiB (100 %)   5.6 MiB/s in  5s ETA:  0s
info: installing component 'rustc'
 67.4 MiB /  67.4 MiB (100 %)   5.9 MiB/s in 11s ETA:  0s
info: installing component 'rustfmt'
info: default toolchain set to 'stable-x86_64-unknown-linux-gnu'

  stable-x86_64-unknown-linux-gnu installed - rustc 1.66.1 (90743e729 2023-01-10)


Rust is installed now. Great!

To get started you may need to restart your current shell.
This would reload your PATH environment variable to include
Cargo's bin directory ($HOME/.cargo/bin).

To configure your current shell, run:
source "$HOME/.cargo/env"

```


### run the following command to add the Rust toolchain directory to the PATH environment variable
``` source $HOME/.cargo/env ```




## If This doesn't work and permission is denied then follow this 

###  Check File Permissions
```  ls -l /home/mohit/.bash_profile ```
here /home/mohit directory address can be found when you type in terminal `pwd`  

If user does not own the file or doesn't have written permission 

`sudo chown mohit /home/mohit/.bash_profile`

Alternative of above 
`chmod u+w /home/mohit/.bash_profile`

#### If .bash_profile Doesn’t Exist
create manually 
`touch ~/.bash_profile`

After creating the file, make sure it has the correct ownership and permissions:
`chown mohit ~/.bash_profile
chmod u+w ~/.bash_profile`

#### Modify Another Shell Profile
` nano ~/.bashrc `

Then add the following lines at the end of the file:
` export PATH="$HOME/.cargo/bin:$PATH" `

#### Bypass the Profile Update
` curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y `

Then manually add the required line to your profile:
` echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bash_profile `

or to another profile like .bashrc:
` echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc `

Finally, reload the profile to apply the changes:
` source ~/.bash_profile `
or 
` source ~/.bashrc `





