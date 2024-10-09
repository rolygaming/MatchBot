<h1 align="center">CS Match BOT</h1>
<p align="center">Counter-Strike 1.6 Match BOT Plugin for Metamod</p>

<p align="center">
    <a href="https://github.com/SmileYzn/MatchBot/issues"><img alt="GitHub Issues" src="https://img.shields.io/github/issues-raw/smileyzn/MatchBot?style=flat-square"></a>
    <a href="https://github.com/SmileYzn/MatchBot/actions"><img alt="GitHub Workflow Status" src="https://img.shields.io/github/actions/workflow/status/SmileYzn/MatchBot/build.yml?branch=main&label=Build Status&style=flat-square"></a>
    <a href="https://github.com/SmileYzn/MatchBot/releases/latest"><img src="https://img.shields.io/github/downloads/SmileYzn/MatchBot/total?label=Download%40latest&style=flat-square&logo=github&logoColor=white" alt="Download"></a>
</p>

<h3>Descripción</h3>
<p>
Este mod permite que el servidor ejecute una partida completa sin que ningún administrador controle el servidor.<br>
Los jugadores deben elegir un equipo, por ejemplo, listo en el chat y esperar a que el servidor comience la partida, o simplemente esperar a que termine el contador de tiempo.<br>
Al final, el servidor iniciará un mapa de votación para cambiar de nivel al siguiente mapa automáticamente.<br>
</p>

<h3>Requisitos</h3>
<ul>
<li>ReHLDS</li>
<li>ReGameDLL_CS</li>
<li>Metamod</li>
</ul>

<h3>Características</h3>
<ul>
<li>Sistema de preparación automático (basado en temporizador como CS:GO o método de sistema de preparación)</li>
<li>Cambios de configuración personalizados entre estados de partida</li>
<li>Gestión de espacios de servidor con soporte para espectadores y espacios de HLTV</li>
<li>Bloqueo automático de jugadores que usan la ira para salir del juego</li>
<li>LO3 automático (activo en tres reinicios)</li>
<li>Balanceador automático de equipos (los jugadores se equilibran cuando ingresan al juego)</li>
<li>Compatibilidad con jugadores bloqueados, elegir equipos o finalizar directamente en el juego</li>
<li>Muchos comandos para que el administrador controle el servidor de partida y los jugadores</li>
<li>Jugadores requeridos configurables para comenzar la partida, también jugadores mínimos para detener si los jugadores se fueron</li>
<li>Juego basado en reglas de rondas máximas (como MR15)</li>
<li>Regla de tiempo extra de soporte de mod, muerte súbita o final directo (en caso de empate)</li>
<li>Un sistema completo de ayuda para jugadores (.help) y administradores (!help)</li>
<li>Comandos de jugador y administrador en el chat o la consola</li>
<li>Rondas de calentamiento con algo de juego de combate a muerte</li>
<li>Lista de mapas personalizada para votar por el próximo mapa, equipos y más</li>
<li>El mod admite la votación de expulsión del jugador, pausa de tiempo de espera, votación de mapa, rendición (votación de fin de partida)</li>
<li>Admite la selección de capitán, balance aleatorio, balance por habilidad desde el calentamiento, cambio de equipos o ronda de kinfe</li>
<li>Admite el mejor de x rondas al inicio para determinar quién ganará la primera ronda (como MD3)</li>
<li>Muestra las estadísticas de daño de la ronda con algunos comandos como .dmg, .hp o .sum y otros</li>
<li>Compatibilidad con varios idiomas</li>
<li>Sistema de banderas de administrador minimalista para gestionar a los administradores en el juego</li>
<li>Compatibilidad con Dead Talk (los compañeros de equipo muertos pueden hablar)</li>
<li>Anti Flood para mensajes de chat y radio</li>
<li>El mod se ejecuta en ReHLDS con el servidor ReGameDLL_CS</li>
<li>Match BOT puede ejecutarse en servidores Windows o Linux</li>
<li>Configuración de servidor personalizada para Optimiza el juego</li>
<li>Puedes ver otras funciones que no aparecen aquí en tu wiki</li>
</ul>

<h3>Match BOT Server Variables</h3>

<details>
  <summary>Click to expand</summary>

| Matchbot.cfg commands list         |  Default value | Description                                    |
| :--------------------------------- | :-----:  | :--------------------------------------------- |
| mb_log_tag                         | BOT      | Match BOT Log Tag. <br/>Here you can put any tag you wish.|
| mb_language                        | en       | Match BOT Language. <br/>`en` English US. <br/>`bp` Brazilian Portuguese.<br/>`es` Spanish Spain.<br/> `ru` Russian RU.<br/> You can edit/create more languages in matchbot\language.json |
| mb_admin_prefix                    | !       | Match BOT administrator command game chat prefix. <br /> For example `!menu` opens administrator menu. |
| mb_player_prefix                   | .       | Match BOT player command game chat prefix. <br /> For example `.dmg` show damage when player dead. |
| mb_players_min                     | 10      | Minimum players needed to start match. |
| mb_players_max                     | 10      | Maximum allowed players in match. |
| mb_play_rounds                     | 30      | Rounds to play before execute overtime.|
| mb_play_rounds_ot                  | 6       | Round to play in overtime. |
| mb_play_ot_mode                    | 3       | Overtime type. <br /> `0` Sudden death round. <br /> `1` Play overtime. <br /> `2` End match tied. <br /> `3` Users vote. |
| mb_ready_type                      | 1       | Ready system type.<br /> `0` Disabled. <br /> `1` Ready System. <br /> `2` Ready Timer. |
| mb_ready_time                      | 60      | Ready system timer delay in seconds. <br /> Only works with `mb_ready_type 2` |
| mb_team_pick_type                  | -1      | Team pickup type when match begin. <br /> `-1` Enable vote. <br /> `0` Leaders. <br /> `1` Random. <br /> `2` None. <br /> `3` Skill balanced. <br /> `4` Swap teams. <br /> `5` Knife round.|
| mb_team_pick_menu                  | abcdef   | Only works with `mb_team_pick_type -1`. <br/>This allows you to make your team pickup menu.<br/> `0` Leaders. <br /> `b` Random. <br /> `c` None. <br /> `d` Skill balanced. <br /> `e` Swap teams. <br /> `f` Knife round|
| mb_vote_map_type                   | 1        | Vote map type. It lets players to choose map or play random map. <br /> `1` Vote map. <br /> `2` Random map. |
| mb_vote_map_auto                   | 2        | Start vote map at match end. <br /> `0` Disabled. <br /> `1` Enabled. <br /> `2` Only when minimum players reached. |
| mb_vote_map_fail                   | 1        | Actions to perform when votemap fails. <br /> `0` Continue match. <br /> `1` Restart vote map. <br /> `2` Choose random map. |
| mb_knife_round                     | 0        | Play Knife Round to choose starting sides. <br /> `0` Disabled. <br /> `1` Enabled.|
| mb_score_type                      | 0        | Scores display method. <br /> `0` Default scores with phrases. <br /> `1` Show all teams and scores. |
| mb_scoreboard_team                 | 1        | Store team scores in scoreboard. <br /> `0` Disabled. <br /> `1` Enabled.|
| mb_scoreboard_player               | 1        | Store player scores in scoreboard. <br /> `0` Disabled. <br /> `1` Enabled.|
| mb_gamename                        | 1        | Display states and scores at game description. <br /> `0` Disabled. <br /> `1` Enabled.|
| mb_player_vote_kick                | 5        | Mininum of players in a team to enable vote kick command for players. <br /> Set to `0` to disable vote kick command.|
| mb_player_vote_map                 | 5        | Mininum of players in a team to enable vote map command for players. <br /> Set to `0` to disable vote map command.|
| mb_player_vote_pause               | 5        | Mininum of players in a team to enable vote pause command for players. <br /> Set to `0` to disable vote pause command.|
| mb_player_vote_restart             | 5        | Mininum of players in a team to enable vote kick command for players. <br /> Set to `0` to disable vote restart command.|
| mb_player_vote_surrender           | 5        | Mininum of players in a team to enable vote kick command for players. <br /> Set to `0` to disable vote surrender command.|
| mb_round_end_stats                 | 0        | Show round stats on end. <br /> `0` Disabled. <br /> `1` Show round damage in chat. <br /> `2` Show round summary in chat. <br /> `3` Show round damage in console. <br /> `4` Show round summary in console. |
| mb_stats_commands                  | abcd     | Enabled round stats commands in chat. <br /> `a` Enable `.hp` command. <br /> `b` Enable `.dmg` command. <br /> `c` Enable `.rdmg` command. <br /> `d` Enable `.sum` command.|
| mb_restrict_weapons                |000000000000000000000000000000000000000| Restricted Weapons by item index slot position (1 to block item, 0 to allow). <br />`0` Shieldgun. <br /> `1` P228. <br /> `2` Glock. <br /> `3` Scout. <br /> `4` Hegrenade. <br /> `5` Xm1014. <br /> `6` C4. <br /> `7` Mac10. <br /> `8` Aug. <br /> `9` Smokegrenade. <br /> `10` Elite. <br /> `11` Fiveseven. <br /> `12` Ump45. <br /> `13` Sg550. <br /> `14` Galil. <br /> `15` Famas. <br /> `16` Usp. <br /> `17` Glock18. <br /> `18` Awp. <br /> `19` Mp5n. <br /> `20` M249. <br /> `21` M3. <br /> `22` M4a1. <br /> `23` Tmp. <br /> `24` G3sg1. <br /> `25` Flashbang. <br /> `26` Deagle. <br /> `27` Sg552. <br /> `28` Ak47. <br /> `29` Knife. <br /> `30` P90. <br /> `31` Nvg. <br /> `32` Defusekit. <br /> `33` Kevlar. <br /> `34` Assault. <br /> `35` Longjump. <br /> `36` Sodacan. <br /> `37` Healthkit. <br /> `38` Antidote. <br /> `39` Battery. |
| mb_extra_smoke_count               | 2        | Extra Smokegranade explosion fix .<br /> `0` Disabled. <br /> `n` Number of extra smoke puffs. |
| mb_pause_time                      | 60.0     | Amount of seconds to pause match. <br /> `0` Disabled. <br /> `n` Or number of seconds to pause the match. |
| mb_retry_mode                      | 0        | Anti reconnect mode. <br /> `0` Disabled. <br /> `1` Enable when player explicity drop from server. <br /> `2` Enable for any disconnect reason. |
| mb_retry_time                      | 30.0     | Anti reconnect time  <br /> Time in seconds to prevent the player reconnect to server |
| mb_help_file                       | cstrike/addons/matchbot/users_help.html     | Users Help File or Website url (Without HTTPS). <br /> If is website url, works only with HTTP (Not HTTPS).|
| mb_help_file_admin                 | cstrike/addons/matchbot/admin_help.html      | Admin Help File or Website url (Without HTTPS). <br /> If is website url, works only with HTTP (Not HTTPS).|
| mb_cfg_match_bot                   | matchbot.cfg  | Match Bot main config. <br /> Executed when Match Bot loads at new map.|
| mb_cfg_warmup                      | warmup.cfg    | Warmup config. <br /> Executed at Warmup session.|
| mb_cfg_start                       | start.cfg     | Start config. <br /> Executed when vote system starts vote teams or vote map.|
| mb_cfg_1st                         | esl.cfg       | First Half config. <br /> Executed when match is live at first half.|
| mb_cfg_halftime                    | halftime.cfg  | Half Time config. <br /> Executed when match is in half time.|
| mb_cfg_2nd                         | esl.cfg       | Second Half config. <br /> Executed when match is live at second half.|
| mb_cfg_overtime                    | esl-ot.cfg    | Overtime config. <br /> Executed at overtime extras rounds.|
| mb_cfg_end                         | end.cfg       | End config. <br /> Executed right after match ends.|
</details>

<h3>¿Por qué CS 1.6 es una porquería?</h3>
<p>
En primer lugar, ¡de nada!<br>
En realidad, tenemos CS:GO, una versión más moderna del juego.<br>
Pero aún podemos divertirnos con un juego como Counter-Strike que se ha jugado durante más de 20 años.<br>
Creo que puedo ayudar a la comunidad a tener más servidores limpios que quieran jugar una partida competitiva.
</p>

<h3>¡Necesito ayuda!</h3>
<p>Visita tu <a href="https://chat.whatsapp.com/JaoNAAEYe11Kw74ygnLZWp">Nuestro Grupo de WhatsApp:</a> para saber qué más puedes hacer con ROLIGAMING MiX</p>
<p>Antes de abrir un problema, asegúrate de haber actualizado ReHLDS Server, ReGameDLL_CS, AMX Mod X y ReAPI.</p>
