create database lanjukang;

migrate -path db/migration -database "postgresql://din:postgres@localhost:5432/lanjukang?sslmode=disable" -verbose up 

jika terjadi masalah pada kode 
- fix masalahnya
- migrate -path db/migration -database "postgresql://din:postgres@localhost:5432/lanjukang?sslmode=disable" -verbose force angka(misalnya 1)
- migrate -path db/migration -database "postgresql://din:postgres@localhost:5432/lanjukang?sslmode=disable" -verbose up

key is of invalid type karena pake secret key string harusnya []byte

token tidak mau diparse karena interface{}
claims["id"].(float64) untuk ubahh interfcae{} menjadi float64
lalu ubah float64 menjadi int dengna int(claims["id"].(float64)) 

untuk handle data yang bisa null dapat pake
 - sql.NUll sting tapi ini susah di unmarshal
 - *string ini leih muda


todo

ubah type decription ke text

buat fungsi ubag role user

tambah tipe data sort description

bagaimana caranya mereturn map dan comment 

pastiakn image terhapus jika gagal create services
pastikan image terhapus jika update
pastikan image terhapus jika delete

Lanjukang@21

jadikan fungsi uploda file go routine

cek apakah updated db ada efek dan tidak null

Lama sekali urus time data
- request dari front end harus sting jadi harus pake struk kusus
- lalu string harus di ubah ke time.Time

perbaiki retun error ke frontedn

update relasi databse - hapus fk dari locasi