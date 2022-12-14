# Crypto
Домашнее задание по криптографии
Алгоритмы шифратор-дешифратор: RSA, SHA-512.
Для того чтобы проиллюстрировать как работает хэширование и подпись с библиотекой rsa были созданы три файла :
Createkeys(для создания открытого и закрытого ключа) с ассиметричным шифрованием .

И система шифрования RSA считается надежной , начиная с размера ключа 2048 бит, поэтому такой и указан.

hashmassage( для подписания хэша и подписать его закрытым ключом )
Decryptall(расшифровывает правильно или нет )
Открытый и закрытый ключи сохраняются в отдельные файлы
В hashmessage изначально мы создаем закрытый ключ
Далее берём сообщение которое мы записали в файл message.
SHA-2 (Secure Hash Algorithm 2) — одно из самых популярных семейств алгоритмов хеширования.SHA-512 устанавливает дополнительные константы, которые определяют поведение алгоритма SHA-2.
SHA-512 будет тратить на четверть больше раундов (80 против 64), чем SHA-256. Но каждый раунд у SHA-512 обрабатывает 64 битовые операнды, а у SHA-256 – 32х битовые. Удвоенное КПД по операндам в сочетании с гарантированной потерей четверти скорости на дополнительных раундах даст 2 / (5/4) = 1.6 раз преимущества.
SHA-512 очень близок к SHA-256, за исключением того, что он использует 1024 битные «блоки» и принимает в качестве входных данных длину строки длиной 2 ^ 128 бит.
для SHA-512 слова имеют длину 64 бита,
используется 80 раундов вместо 64,
Далее создаем хэш для этого сообщения. При помощи алгоритма SHA-512., Это означает что мы собираемся создать цифровую печать этого файла, чтобы показать что он не был изменен.
И создаем подпись и сохраняем файл подписи в файл.
В файле decrypt мы открываем наш открытый ключ, чтобы убедиться что подпись закрытого ключа уместна. Открываем наше сообщение и файл подписи. Далее запускаем библиотеку rsa verify чтобы убедиться в правильности написания. Если возникают проблемы с проверкой, то выходит предупреждение
