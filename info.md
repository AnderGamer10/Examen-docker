Para el balanceador de carga-------------------------------

upstream load_balance {
        server web1;
        server web2;
    }

server{
    listen 80;
    listen [::]:80;
    server_name localhost;

    location / {
        proxy_pass http://load_balance;

}
}



Para el proxy-------------------------------

server{
    listen 80;
    listen [::]:80;
    server_name localhost;

    location /s1 {
        root /usr/share/nginx/html;
        proxy_pass http://web1/;
    }

    location /s2 {
        root /usr/share/nginx/html;
        proxy_pass http://web2/;
    }
}



