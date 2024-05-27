# Gunakan image dasar nginx
FROM nginx:latest

# Hapus konfigurasi default nginx
RUN rm /etc/nginx/conf.d/default.conf

# Salin file konfigurasi nginx ke dalam container
COPY nginx.conf /etc/nginx/conf.d/

# Salin file HTML ke dalam direktori yang akan dilayani oleh nginx
COPY index3.html /usr/share/nginx/html/

# Ekspose port 80
EXPOSE 80

# Perintah default untuk menjalankan nginx
CMD ["nginx", "-g", "daemon off;"]
