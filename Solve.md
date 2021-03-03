# ИБиЗИ
Лабораторная работа №2  
Номер зачетки: 1800189
# Задания
1. Создайте текстовый файл содержащий вашу фамилию и имя. (скриншот в отчет)  
`cat > textfile`  
`Iskander Khisamov`  
`Ctrl-Z`
2. Вычислите хеш для этого файла алгоритмами MD4, MD5, SHA, SHA512. (скриншоты в отчет)  
`openssl dgst -md4 textfile`  
`openssl dgst -md5 textfile`  
`openssl dgst -sha1 textfile`  
`openssl dgst -sha512 textfile`
3. Измените содержимое файла, вычислите хеши, сравните с предыдущим хешами. (скриншоты в отчет)  
`cat > textfile`  
`Iskander Khisamov Ravilevich`  
`Ctrl-Z`  
`openssl dgst -md4 textfile`  
`openssl dgst -md5 textfile`  
`openssl dgst -sha1 textfile`  
`openssl dgst -sha512 textfile`
4. Вычислите хеш для большого файла (файл у всех разный) алгоритмами MD4, MD5, SHA, SHA512 засекая время выполнения (команда time). (скриншоты в отчет)  
`fallocate -l 1G bigfile`  
`time openssl dgst -md4 bigfile`  
`time openssl dgst -md5 bigfile`  
`time openssl dgst -sha1 bigfile`  
`time openssl dgst -sha512 bigfile`
5. Вычислите имитовставку, используя алгоритм SHA512, для текстового файла с разными ключами, сравните результаты. (скриншоты в отчет)  
`cat > text.txt`
`Live Text`
`Ctrl-Z`  
`openssl dgst -sha512 -mac HMAC -macopt hexkey:123456 text.txt`  
`openssl dgst -sha512 -mac HMAC -macopt hexkey:7890 text.txt` 
6. Получите имитовставку для текстового файла с разными ключами, имитовставка длиной N байт (N-последняя цифра в зачетке), в формате base64, используя алгоритм DES-CBC, сравните результаты. (скриншоты в отчет)  
``   
# Теория
1. хеширование
2. имитовставка (принцип вычислений и области применения)
3. разобрать сравнительно алгоритмы MD5, SHA, ГОСТ Р 34.11-94, ГОСТ Р 34.11-2012.
