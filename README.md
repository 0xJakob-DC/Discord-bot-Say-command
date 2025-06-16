# Discord-bot-Say-command
Your average Discord bot's "Say" command is right here! 

# Remember to use python for this code to work!
(open the README so it works to copy)
**You also need a "On ready" event:**

@client.event
async def on_ready():
    print(f'Logged in as {client.user}')
    try:
        synced = await client.tree.sync()
        print(f"synced {len(synced)} command(s))")
        print("-------------------------------")
    except Exception as e:
        print(e)
