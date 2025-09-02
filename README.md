# DiscordWebSync---Vincule-Minecraft-com-Discord

RESUMO

O DiscordWebSync integra seu servidor Minecraft ao Discord de forma segura, permitindo vinculação de contas e comunicação automatizada.

🔧 Configurações no config.yml

discordBotToken: Token do bot do Discord (não está mais no código-fonte, apenas no config).

discordChannelId: ID do canal do Discord onde as mensagens serão enviadas.

📜 Comandos Disponíveis /setdiscord

Registra o Discord do jogador no servidor.

Necessário para receber códigos e vincular contas.

Salva informações no banco SQLite e no banco.yml.

Bloqueado se o jogador já tiver ativado um código.

/conectar

Gera um código exclusivo para o jogador.

Envia o código diretamente no canal do Discord especificado.

Salva data e hora da execução.

Só pode ser usado por jogadores que registraram o Discord com /setdiscord.

/vincular

Confirma que o código foi liberado e está pronto para ser ativado.

Apenas visual; não gera códigos.

Exige que o jogador tenha usado /conectar antes.

/ativar_codigo

Ativa o código previamente gerado e vincula a conta Minecraft ao Discord.

Marca o código como usado e salva data e hora da ativação.

Envia mensagem no canal do Discord informando que a conta foi vinculada.

Bloqueado se o código já tiver sido usado ou se o jogador já estiver vinculado.

/discord

Exibe o link do Discord do servidor diretamente no chat do Minecraft.

🔒 Segurança e Controle

Apenas o jogador que registrou seu Discord via /setdiscord pode receber códigos.

Comandos bloqueados automaticamente se o jogador já tiver um código ativado.

Sistema de cooldown de 5 minutos para evitar spam de códigos.

Token do bot armazenado apenas no config.yml, nunca no código.

🗄️ Banco de Dados e Logs Banco de Dados

SQLite (banco_aux.db): inclui UUID, DiscordID, código, usado e data/hora.

YML (banco.yml): backup para fácil consulta.

Logs Detalhados

/logs/info/info.log → Informações gerais.

/logs/warning/warning.log → Alertas ou tentativas indevidas.

/logs/error/error.log → Erros graves e falhas do sistema.
