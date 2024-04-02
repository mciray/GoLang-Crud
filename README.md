# Go REST API Örneği

Bu proje, PostgreSQL veritabanını kullanan basit bir Go REST API'sidir. CRUD işlemleri için basit bir `Item` modeli üzerinde çalışır.

## Başlarken

Bu bölüm, projeyi yerel makinenizde çalıştırmanız için gerekli ön koşulları ve kurulum adımlarını içerir.

### Önkoşullar

Projeyi çalıştırmak için aşağıdakilere ihtiyacınız olacak:

- Go (1.15 veya üzeri)
- PostgreSQL
- Git

### Kurulum

1. Projeyi klonlayın:
```bash
git clone https://github.com/<kullanıcıadı>/<repo-adı>.git
```
2. .env dosyasını oluşturun ve veritabanı bağlantı bilgilerinizi girin:
```bash
    DB_HOST=host
    DB_PORT=port
    DB_USER=user
    DB_PASSWORD=password
    DB_NAME=db_name
```
3. Gerekli Go paketlerini yükleyin:
```bash
    go get -u github.com/lib/pq
    go get -u github.com/gorilla/mux
    go get -u github.com/joho/godotenv
```
4. Uygulamayı başlatın:
```bash
   go run main.go
```
### Kullanım

1. Bu API, temel CRUD işlevlerini gerçekleştirebilir. Örneğin, tüm öğeleri listelemek için:
```bash
curl http://localhost:8080/items
```
2. eni bir öğe eklemek için:
```bash
curl -X POST -H "Content-Type: application/json" -d '{"name":"Yeni Öğe"}' http://localhost:portunuz/item

```

