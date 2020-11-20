# Appku_OAUTH2

Sistem ini dibangunkan untuk implement di agensi seperti Hospital, Kerajaan , Pentadbiran dan Syarikat yang memiliki sistem Internal yang login menggunakan username dan password yang sama di setiap sistem. 

Ini adalah shortcut mengelakkan cara implement di Infra. 

Engine auth digunakan memudahkan user tidak perlu nak login hanya dengan menggunakan 1 klik button boleh akses mana-mana 
website yang sah dengan token yang ada

- Langkah 1 : Create Folder - piiyel19
- Langkah 2 : setup server.php - attach dengan db local
- Langkah 3 : Request token - mesti di insert terlebih dahulu seperti validkan user dalam sistem kita 

INSERT INTO oauth_clients (client_id, client_secret, redirect_uri) VALUES ("testclient", "testpass", "http://url_kalau_failed_macam_callback/");

Langkah 4 : Test Authorized 

Langkah 5 : Boleh call panggil -> http://localhost/oauth2/piiyel19/authorize.php?response_type=code&client_id=testclient&state=xyz

data pass di periksa kat engine auth 
kalau valid dia akan pergi kemana yang disarankan (authorize.php)


Note : Biasa di implement kalau ada banyak sistem dalam 1 server Internal sangat sesuai implement sistem macam ni seperti Hospital, Agensi Gov
