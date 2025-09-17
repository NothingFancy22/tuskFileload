location /ws/ {
            proxy_pass $scheme://192.168.10.156:6652;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection "upgrade";
            proxy_set_header Host $host;
            proxy_set_header Origin $http_origin;
            #proxy_cache_bypass $http_upgrade;
        }
