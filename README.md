# Discord-bot-Say-command
Your average Discord bot's "Say" command is right here! 

# Remember to use python for this code to work!

You also need a "On ready" event:

@client.event
async def on_ready():
    print(f'Logged in as {client.user}')
    await client.change_presence(status=discord.Status.online, activity=discord.Activity(type=discord.ActivityType.playing , name="x!assist"))
    try:
        synced = await client.tree.sync()
        print(f"synced {len(synced)} command(s))")
        print("-------------------------------")
    except Exception as e:
        print(e)
