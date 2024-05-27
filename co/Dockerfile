# Gunakan image dasar nginx
FROM nginx:latest

# Hapus konfigurasi default nginx
RUN rm /etc/nginx/conf.d/default.conf

# Hapus old HTML
RUN rm /usr/share/nginx/html/index.html

# Salin file konfigurasi nginx ke dalam container
COPY nginx.conf /etc/nginx/conf.d/

# Salin file HTML ke dalam direktori yang akan dilayani oleh nginx
COPY index3.html /usr/share/nginx/html/
RUN mv /usr/share/nginx/html/index3.html /usr/share/nginx/html/index.html

# Salin Gambar
COPY checkout.jpg /usr/share/nginx/html/

# Ekspose port 80
EXPOSE 80

# Perintah default untuk menjalankan nginx
CMD ["nginx", "-g", "daemon off;"]