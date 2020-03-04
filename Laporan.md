
<h1 align="center"><img src="https://www.teeworlds.com/images/twlogo.png"></h1>

* [Sekilas Tentang](#sekilas-tentang) 
* [Instalasi](#instalasi) 
* [Konfigurasi](#konfigurasi) 
	* [Setting](##Setting)
		* [Engine setting](###Engine-setting)
		* [Game setting](###Game-setting)
	* [Tuning](##Tuning)
		* [Physics tuning](###Physics-tuning)
		* [Weapons tuning](###Weapons-tuning)
* [Cara Pemakaian](#cara-pemakaian) 
* [Pembahasan](#pembahasan) 
* [Referensi](#referensi)

# Sekilas Tentang

Teeworlds adalah sebuah game *retro multiplayer sidescrolling shooter* yang gratis dan *open source*.

# Instalasi()

(isi ini fidz)

# Konfigurasi

Tidak seperti aplikasi yang lain, untuk menjalankan server Teeworld harus di atur konfigurasi tersebut.

## Setting

 Berikut adalah setting yang dapat diubah : 

### Engine setting<sup>[1]</sup>
*: tidak bisa diubah selama server berjalan


|Settings|Description|Default|
|--- |--- |--- |
|sv_name|Name of the server|unnamed server|
|bindaddr *|Address to bind||
|sv_port *|Port the server will listen on|8303|
|sv_external_port *|Port to report to the master servers (e.g. in case of a firewall rename)|0|
|sv_max_clients *|Number of clients that can be connected to the server at the same time|12|
|sv_max_clients_per_ip|Number of clients with the same ip that can be connected to the server at the same time|12|
|sv_high_bandwidth *|Use high bandwidth mode, for LAN servers only|0|
|sv_register|Register on the master servers|1|
|sv_map|Map to use|dm1|
|sv_rcon_password|Password to access the remote console (if not set, rcon is disabled)||
|password|Password to connect to the server||
|logfile|Path to a logfile||
|console_output_level|Adjust the amount of messages in the console|0|
|sv_rcon_max_tries|Maximum number of tries for remote console authetication|3|
|sv_rcon_bantime|Time (in minutes) a client gets banned if remote console authentication fails (0 makes it just use kick)|5|
|sv_auto_demo_record|Automatically record demos|0|
|sv_auto_demo_max|Maximum number of automatically recorded demos (0 = no limit)|10|
|ec_bindaddr|Address to bind the external console to. Anything but 'localhost' is dangerous"|localhost|
|ec_port|Port to use for the external console||
|ec_password|External console password"||
|ec_bantime|The time a client gets banned if econ authentication fails. 0 just closes the connection|0|
|ec_auth_timeout|Time in seconds before the the econ authentication times out|30|
|ec_output_level|Adjusts the amount of information in the external console|1|

### Game setting
|Settings|Description|Default|
|--- |--- |--- |
|sv_warmup|Warmup time between rounds|0|
|sv_scorelimit|Score limit of the game (0 disables it)|20|
|sv_timelimit|Time limit of the game (in case of equal points there will be sudden death)|0|
|sv_gametype|Gametype (dm/ctf/tdm/lms/lts) (This setting needs the map to be reloaded in order to take effect)|dm|
|sv_maprotation|The maps to be rotated||
|sv_rounds_per_map|Number of rounds before changing to next map in rotation|1|
|sv_motd|Message of the day, shown in server info and when joining a server||
|sv_player_slots|Number of slots to reserve for players. Replaces "svspectatorslots"|8|
|sv_teambalance_time|Time in minutes after the teams are uneven, to auto balance|1|
|sv_spamprotection|Enable spam filter|1|
|sv_tournament_mode|Players will automatically join as spectator|0|
|sv_player_ready_mode|When enabled, players can pause/unpause the game and start the game on warmup via their ready state|0|
|sv_strict_spectate_mode|Restricts information like health, ammo and armour in spectator mode|0|
|sv_silent_spectator_mode|Mute join/leave message of spectator|1|
|sv_skill_level|Skill level shown in serverbrowser (0 = casual, 1 = normal, 2 = competitive)|1|
|sv_respawn_delay_tdm|Time needed to respawn after death in tdm gametype|3|
|sv_teamdamage|Enable friendly fire|0|
|sv_powerups|Enable powerups (katana)|1|
|sv_respawn_delay_tdm|Enable powerups (katana)|1|
|sv_vote_kick|Enable kick voting|1|
|sv_vote_kick_bantime|Time in minutes to ban a player if kicked by voting (0 equals only kick)|5|
|sv_vote_kick_min|Minimum number of players required to start a kick vote|0|
|sv_inactivekick_time|Time in minutes after an inactive player will be taken care of|3|
|sv_inactivekick|How to deal with inactive players (0 = move to spectator, 1 = move to free spectator slot/kick, 2 = kick)|1|
|sv_vote_spectate|Allow voting to move players to spectators|1|
|sv_vote_spectate_rejoindelay|How many minutes to wait before a player can rejoin after being moved to spectators by vote|3|

## Tuning

Tuning hanya dapat bisa diubah jika gametype nya bukan vanilla. Jika ingin diganti, set gametype menjadi mod dengan sv_gametype mod.<sup>[2]</sup>

### Physics tuning
|Tuning|Description|Default|Unit|
|--- |--- |--- |--- |
|ground_control_speed|Max speed the tee can get on ground|10.0||
|ground_control_accel|Acceleration speed on the ground|2.0||
|ground_friction|Friction on the ground|0.5||
|ground_jump_impulse|Impulse when jumping on ground|13.2||
|air_jump_impulse|Impulse when jumping in air|12.0||
|air_control_speed|Max speed the tee can get in the air|5.0||
|air_control_accel|Acceleration speed in air|1.5||
|air_friction|Friction in the air|0.95||
|hook_length|Length of the hook|380.0|pixels|
|hook_fire_speed|How fast the hook is fired|80.0||
|hook_drag_accel|Acceleration when hook is stuck|3.0||
|hook_drag_speed|Drag speed of the hook|15.0||
|gravity|Gravity of the teeworld|0.5||
|velramp_start|Velocity ramp start|550.0||
|velramp_range|Velocity ramp range|2000.0||
|velramp_curvature|Velocity ramp curvature|1.4||
|player_collision|Enable player collisions|1||
|player_hooking|Enable player vs player hooking|1||
### Weapons tuning
|Tuning|Description|Default|Unit|
|--- |--- |--- |--- |
|gun_curvature|Gun curvature|1.25||
|gun_speed|Gun speed|2200.0|pixels / sec|
|gun_lifetime|Gun lifetime|2.0|sec|
|shotgun_curvature|Shotgun curvature|1.25||
|shotgun_speed|Shotgun speed|2750.0|pixels / sec|
|shotgun_speeddiff|(UNUSED) Speed difference between shotgun bullets|0.8||
|shotgun_lifetime|Shotgun lifetime|0.20|sec|
|grenade_curvature|Grenade curvature|7.0||
|grenade_speed|Grenade speed|1000.0|pixels / sec|
|grenade_lifetime|Grenade lifetime|2.0|sec|
|laser_reach|How long the laser can reach|800.0|pixels|
|laser_bounce_delay|When bouncing, stop the laser this long|150.0|ms|
|laser_bounce_num|How many times the laser can bounce|1.0||
|laser_bounce_cost|Remove this much from reach when laser is bouncing|0.0|pixels|
|laser_damage|Laser damage|5.0|damage|




# Cara Pemakaian ()

- Tampilan aplikasi web
- Fungsi-fungsi utama
- Isi dengan data real/dummy (jangan kosongan) dan sertakan beberapa screenshot

Buka aplikasi client Teeworlds yang sudah di download

# Pembahasan ()

- Pendapat anda tentang aplikasi web ini
    - kelebihan
    - kekurangan
- Bandingkan dengan aplikasi web lain yang sejenis


# Referensi

[1] : https://www.teeworlds.com/?page=docs&wiki=server_settings

[2] : https://www.teeworlds.com/?page=docs&wiki=server_tuning
