import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='#', intents=intents)

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hola(ctx):
    await ctx.send(f'Hola, soy un bot, y te voy a ayudar a disminuir el uso de plastico en tu día a día. Si quieres saber como disminuir el uso de este material, escribe "uno". Si quieres saber como afecta el plastico a nuestro planeta, escribe "dos". Si quieres saber como el uso plástico puede llegar a afectarnos escribe "tres".')

@bot.command()
async def uno(ctx):
    await ctx.send(f'Hay muchas diferentes maneras de disminuir el uso del plastico en tu día a día: ')
    await ctx.send(f'1. Por ejemplo, a veces, cuando tenemos sed, lo primero que pensamos es en comprar una botella de plastico. Esto, ademas de ser dañino, puede ser evitado. Si todos empezamos a llevar nuestra propia botella a todas partes, no solo nos ahorraremos una gran cantidada de dinero, si no que tambien estaremos salvando de alguna u otra manera a muchos animales.')
    await ctx.send(f'2. Otra opcion es simple mente evitar comprar cosas de este material. Ahora, auque esta tarea pueda ser algo dificil, no es necesario parar por completo la compra d este material. Sin embrgo, podemos para de comprarlo para cosas inecesarias. Algunos ejemplos son lo vasos, platos, y cubiertos de plastico.')
    await ctx.send(f'3. La tercera opcion es usar el plastico que usas a diario para hacer manualidades. Esto ademas de ser divertido puede ser muy eficiente! Ya que al hacer una maceta, o algo asi, no solo te entretienes, si no que tambien puedes ayudar a limpiar un muy pequeño porcentaje de aire! ')



@bot.command()
async def dos(ctx):
    await ctx.send(f'Estas son algunas de las maneras en las que el plastico afecta a nuestro planeta:')
    await ctx.send(f'1. EL plástico no se degrada facilmente. Puede tardar cientos o miles de años en decomponerse, acumulándose en ríos, oceanos, suelos y paisajes naturales. Con el tiempo este se fragmentará en partículas muy pequeñas llamadas microplásticos, que termina en el agua, el aire y hasta en los alimentos que consumimos.')
    await ctx.send(f'2. Muchas especies (tortugas, aves, peces, etc.) confunden el plástico con comida y lo ingieren. Esto puede causar asfixia, bloqueos intestinales y muerte. Otros animales pueden quedar atrapados en redes, bolsas o anillos de plástico, esto les impide moverse o alimentase.')
    await ctx.send(f'3. La fabricación de plástico utiliza combustibles fósiles, lo que genera emisiones de efecto invernadero. Cuendo el plástico se quema con basura, libera gases y contribuye al calentamiento global.')
    await ctx.send(f'4. En muchos lugares, el plástico no se recicla correctamente y termina en vertederoso tirado al aire libre. A través de la lluvia, el plástico puede llegar a ríos y mares, empeorando la contaminación hídrica.')

@bot.command()
async def tres(ctx):
    await ctx.send(f'Estas son algunas de las maneras en las que el plástico llega a afectarnos:')
    await ctx.send(f'1. Al comer pescado, sal, agua embotellada o incluso respirar, estamos consumiendo microplásticos. Aún se está estudiando el efecto exacto, pero ya se sospecha que pueden causar inflamación y estrés celular. Además, algunos plásticos liberan substancias tóxicas que pueden afectar al sistema hormonal, al cerebro o incluso estar relacionada con ciertos tipos de cancer.')
    await ctx.send(f'2. El uso de plásticos para calentar comida o almacenar alimentos puede liberar químicos nocivos, especialmente si el plástico no es apto para altas temperaturas. ')
    await ctx.send(f'3. Vivir en lugares llenos de basura plástica no solo es desagradable, también aumenta el riesgo de enfermedades y afecta la calidad de vida.')
    await ctx.send(f'4. Las playas y ríos contaminados con plástico pueden ahuyentar turistas y afectar a comunidades que dependen de esas actividades.')


bot.run("token")
