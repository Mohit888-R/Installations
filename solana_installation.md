### Solana Installation 
Step 1 : Open your terminal 

Step 2 : Install the Solana release v1.18.18 on your machine by running:
      ` sh -c "$(curl -sSfL https://release.solana.com/v1.18.18/install)" `

Step 3 : solana --version


### Download Prebuilt Binaries

Instructions: If you would rather not use solana-install to manage the install, you can manually download and install the binaries.

Step 1  : Download the binaries by navigating to https://github.com/solana-labs/solana/releases/latest, download solana-release-x86_64-unknown-linux-gnu.tar.bz2,

Step 2 : Go to download zip file path

Step 3 : then extract the archive:
      ` tar jxf solana-release-x86_64-unknown-linux-gnu.tar.bz2
        cd solana-release/
        export PATH=$PWD/bin:$PATH`

