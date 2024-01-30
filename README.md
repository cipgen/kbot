## Golang Installation and Development Environment Setup
- **Note:** Codespaces already includes all necessary settings.

### GitHub Project Creation and Git Configuration
```bash
echo "# kbot" >> README.md       # Create and write to README.md
git init                        # Initialize a new Git repository
git add README.md               # Add README.md to the staging area
git commit -m "first commit"    # Commit the changes with a message
git branch -M main              # Rename the current branch to 'main'
git remote add origin https://github.com/cipgen/kbot.git # Add a new remote repository
git push -u origin main         # Push changes to the remote repository and set upstream
Adding Dependency on github.com/spf13/cobra
Demonstrated in lecture 2.4.
bash
Copy code
go install github.com/spf13/cobra-cli@latest  # Install cobra-cli
cobra-cli init                                # Initialize a new Cobra application
Go Import Statement
go
Copy code
import (
    "github.com/spf13/cobra"  # Import the cobra package
)
Creating a Telegram Bot using BotFather
Instructions to create a new bot named 'kbot' using BotFather.
Bot Token Handling
bash
Copy code
read -s TELE_TOKEN   # Read the bot token securely and store in TELE_TOKEN
Importing Libraries and Installing gopkg.in/telebot.v3
bash
Copy code
go get -u gopkg.in/telebot.v3   # Fetch the telebot package and its dependencies
gofmt -s -w ./                  # Format the Go code in the current directory
go get                          # Download and install packages and dependencies
Retrieving the Bot Token from the Environment Variable
bash
Copy code
echo $TELE_TOKEN    # Display the value of TELE_TOKEN
export TELE_TOKEN   # Export the token as an environment variable
Creating a Bot Object with telebot.NewBot()
go
Copy code
kbot, err := telebot.NewBot(telebot.Settings{ 
    URL: "", 
    Token: TeleToken, 
    Poller: &telebot.LongPoller{Timeout: 10 * time.Second}, 
})  # Initialize a new telebot with settings
Adding a Message Handler Function
go
Copy code
kbot.Handle(telebot.OnText, func(m telebot.Context) error {
    # ... Handler logic ...
})
Building, Running, and Testing the Bot
bash
Copy code
go build -ldflags "-X="github.com/cipgen/kbot/cmd.appVersion=v1.0.3  # Build the bot with version flag
Creating a README File
Include project description, bot link (t.me/<Bot_Name>_bot), installation instructions, and command examples.
Uploading Code to GitHub
bash
Copy code
go version                         # Check the installed Go version
go mod init github.com/cipgen/kbot # Initialize a new Go module
# ... Additional setup and run commands ...
git add .                          # Add all new and changed files to staging
git commit -m "first app kbot"     # Commit with a message
git branch                         # List branches
git remote -v                      # List remote repositories
git push                           # Push changes to the remote repository
Additional Commands for Bot Functionality and Deployment
bash
Copy code
# ... Commands including `go get`, `gofmt`, `go build`, and running the application ...
vbnet
Copy code

This Markdown format provides a structured and easy-to-follow guide for each step of the process, from setting up the environment to deploying the bot.


________

go get -u gopkg.in/telebot.v3  
gofmt -s -w ./  
go get  
go build -ldflags "-X="github.com/cipgen/kbot/cmd.appVersion=v1.0.1  
./kbot  
./kbot start  
read -s TELE_TOKEN  
echo $TELE_TOKEN  
export TELE_TOKEN  
go build -ldflags "-X="github.com/cipgen/kbot/cmd.appVersion=v1.0.2  


TELE_TOCKEN 6819611883:AAG5my3l9m8KQV1IrjBNw6etNG9VaxgBtfE
```