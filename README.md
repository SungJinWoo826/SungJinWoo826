const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({ 
    intents: [
        GatewayIntentBits.Guilds,
        GatewayIntentBits.GuildMessages,
        GatewayIntentBits.MessageContent
    ] 
});

client.once('ready', () => {
    console.log('¡Bot está listo!');
});

client.on('messageCreate', (message) => {
    if (message.content === '!hola') {
        message.channel.send('¡Hola! ¿Cómo estás?');
    }
});

client.login('TU_TOKEN_DEL_BOT');


