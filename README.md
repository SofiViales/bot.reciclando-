import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hola(ctx):
    await ctx.send(f'Hola, soy un bot, y te voy a ayudar a disminuir el uso de plastico en tu día a día. Si quieres saber como disminuir el uso de este material, escribe "uno". Si quieres saber como afecta el plastico a nuestro planeta, escribe "dos". Si quieres saber que animales se han visro afectados por este escribe "tres".')

@bot.command()
async def uno(ctx):
    await ctx.send(f'Hay muchas diferentes maneras de disminuir el uso del plastico en tu día a día. ')
    await ctx.send(f'1. Por ejemplo, a veces, cuando tenemos sed, lo primero que pensamos es en comprar una botella de plastico. Esto, ademas de ser dañino, puede ser evitado. Si todos empezamos a llevar nuestra propia botella a todas partes, no solo nos ahorraremos una gran cantidada de dinero, si no que tambien estaremos salvando de alguna u otra manera a muchos animales.')
    await ctx.send(f'2. Otra opcion es simple mente evitar comprar cosas de este material. Ahora, auque esta tarea pueda ser algo dificil, no es necesario para por completo la compra d este material. Sin embrgo, podemos para de comprarlo para cosas inecesarias. Algunos ejemplos son lo vasos, platos, y cubiertos de plastico.')
    await ctx.send(f'3.')


@bot.command()
async def dos(ctx):
    await ctx.send(f'')

@bot.command()
async def tres(ctx):
    await ctx.send(f'')
  

bot.run("token")

