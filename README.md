# Discord
I want to know where is my problem. When i ejecute i recive this message "discord.ext.commands.errors.CommandInvokeError: Command raised an exception: RuntimeError: PyNaCl library needed in order to use voice"

i re install the pip discord.py[voice]

I try to use this code:

import discord
from discord.ext import commands

client = commands.Bot(command_prefix="!")

@client.command()
async def play(ctx, url : str):
    voiceChannel = discord.utils.get(ctx.guild.voice_channels, name="General")
    voice = discord.utils.get(client.voice_clients, guild=ctx.guild)
    await voiceChannel.connect()
client.run("TOKEN")
