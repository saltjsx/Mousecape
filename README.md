# Mousecape

A free cursor manager for macOS 10.8+ that allows you to customize your cursor using private CoreGraphics APIs.

![](https://github.com/alexzielenski/Mousecape/raw/master/screenshot.png)

## How to Compile Mousecape on macOS

This guide will walk you through compiling Mousecape from source code, even if you're a complete beginner.

### Prerequisites

Before you start, you'll need to install Xcode (Apple's development tool):

1. **Install Xcode** from the Mac App Store (it's free)
   - Open the **App Store** app on your Mac
   - Search for "Xcode"
   - Click **Get** or **Install** (this may take a while as Xcode is large, ~10-15 GB)
   - Wait for the installation to complete

2. **Install Xcode Command Line Tools**
   - Open the **Terminal** app (find it in Applications → Utilities, or use Spotlight by pressing ⌘+Space and typing "Terminal")
   - Type the following command and press Enter:
     ```bash
     xcode-select --install
     ```
   - Click **Install** when the popup appears
   - Wait for the installation to complete

### Getting the Source Code

3. **Download the source code**
   
   **Option A: Using Git (recommended)**
   - Open Terminal
   - Navigate to where you want to download the code (e.g., your Desktop):
     ```bash
     cd ~/Desktop
     ```
   - Clone the repository:
     ```bash
     git clone https://github.com/saltjsx/Mousecape.git
     ```
   - Navigate into the project folder:
     ```bash
     cd Mousecape
     ```

   **Option B: Download ZIP**
   - Click the green **Code** button on this GitHub page
   - Click **Download ZIP**
   - Extract the ZIP file to your Desktop
   - In Terminal, navigate to the extracted folder:
     ```bash
     cd ~/Desktop/Mousecape-master
     ```

### Compiling the Application

4. **Open the project in Xcode**
   - In Terminal (from the Mousecape folder), type:
     ```bash
     cd Mousecape
     open Mousecape.xcodeproj
     ```
   - Xcode will open with the project loaded

5. **Build the application**
   - In Xcode, at the top left, make sure the scheme dropdown shows **Mousecape** (not mousecloak or mousecloakHelper)
   - Next to it, select **My Mac** as the destination
   - Click the **Play** button (▶️) in the top left, or press ⌘+R
   - The project will compile (this may take a minute)

6. **Find your compiled app**
   - Once the build succeeds, the app will launch automatically
   - To find the compiled .app file:
     - In Xcode, go to **Product** → **Show Build Folder in Finder**
     - Navigate to **Products** → **Debug**
     - You'll find **Mousecape.app** here
   - You can copy this .app file to your Applications folder to use it permanently

### Alternative: Build from Command Line

If you prefer using the command line:

```bash
cd ~/Desktop/Mousecape/Mousecape
xcodebuild -project Mousecape.xcodeproj -scheme Mousecape -configuration Release build
```

The compiled app will be in:
```
~/Desktop/Mousecape/Mousecape/build/Release/Mousecape.app
```

### Troubleshooting

**"No developer tools were found"**
- Run `xcode-select --install` again and make sure it completes

**"Failed to prepare the device for development"**
- This is normal - just ignore it and try building again

**Code signing errors**
- Go to Xcode → Settings → Accounts → Add your Apple ID
- Select the project in Xcode, go to Signing & Capabilities, and choose your development team

**Build fails with errors**
- Make sure you're using a recent version of macOS (10.13+) and Xcode (10+)
- Try cleaning the build: Product → Clean Build Folder (⇧⌘K) and build again

### What's Next?

After compiling:
1. Open the Mousecape app
2. Go to **Mousecape** → **Install Helper Tool** (you'll need to enter your password)
3. Import cursor capes (.cape files) by double-clicking them or dragging them into Mousecape
4. Apply your favorite cursor theme!

## License

Copyright (c) 2013-2014, Alex Zielenski. All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Any redistribution, use, or modification is done solely for personal benefit and not for any commercial purpose or for monetary gain

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
