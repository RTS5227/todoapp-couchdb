Cấu hình

1: Tạo một thư mục chứa các static files, ví dụ /home/`<user>`/www
- cd /home/`<user>`/www
- git clone git@github.com:ltlam93/todoapp-couchdb.git

2: Truy cập http://localhost:5984/_utils/config.html

3: Add a new section

4: Điền vào form như sau
- section: httpd_global_handlers
- option: _www
- value: {couch_httpd_misc_handlers, handle_utils_dir_req, "/home/`<user>`/www"}

5: Restart Couchdb
sudo service couchdb restart

6: Tạo CSDL "tododb"

7: Truy cập http://localhost:5984/_www/ 
