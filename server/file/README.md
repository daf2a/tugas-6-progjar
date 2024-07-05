# Multi-Realm Chat Application

## Dokumentasi

### Repository Tugas di GitHub

[GitHub Repository](https://github.com/herukurniawann/FP_ProgjarKelompok5_Soket)

### Definisi Protokol Chat

#### Private Messaging

Format pesan:

```
send <sessionid> <username_to> <message>
```

Contoh:

```
send abc123 heru Hello, how are you?
```

#### Group Messaging

Format pesan:

```
sendgroup <sessionid> <group_name> <message>
```

Contoh:

```
sendgroup abc123 group1 Hello, everyone!
```

### Definisi Protokol Pertukaran Antar Server Antar Realm

Kirim pesan antar realm:

```
sendrealm <username_from> <username_to> <message>
```

Contoh:

```
sendrealm alice heru Hello from another realm!
```

Kirim pesan grup antar realm:

```
sendgrouprealm <username_from> <group_name> <message>
```

Contoh:

```
sendgrouprealm alice group1 Hello group from another realm!
```

### Arsitektur Implementasi

- **Server 1:**
  - IP Address: `127.0.0.1`
  - Chat Port: `8889`
  - Realm Port: `8890`
- **Server 2:**
  - IP Address: `127.0.0.2`
  - Chat Port: `8888`
  - Realm Port: `8891`
