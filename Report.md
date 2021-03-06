# Отчёт о тестировании установки OpenJDK11 и работы Key Validator

## Краткое описание

28.04.20 было проведено тестирование установки OpenJDK11, а также  функциональное тестирование приложения Key Validator.class

На тестирование затрачено: 0.5 часа

В результате тестирования выявлены следующие дефекты:
* [Валидные ключи для KeyValidator выдают Fail](https://github.com/Ksenia-Ling/JavaHW-1.1/issues/1) 
* [Невалидный ключ для KeyValidator выдаёт Ok](https://github.com/Ksenia-Ling/JavaHW-1.1/issues/3) 

В результате тестирования установки OpenJDK11 дефектов не выявлено.
## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* Инструкция по установке OpenJDK11
* Руководство использования Key Validator
* Баг-репорты
* Отчёт о тестировании


В качестве тестовых данных использовались данные из [инструкции по установке OpenJDK11](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md)

После установки откройте терминал и выполните команду:

```
java -version
```

Ожидаемый результат: вывод подобный 

```
openjdk version "11.0.5" 2019-10-15 

OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.5+10)

OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.5+10, mixed mode)
```

 А также данные из [руководства использования Key Validator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)

Валидные ключи:

- 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998
- 80b427f8-92cd-3aae-ba04-3927fbe17c6
- b295bc63-9f03-3b4b-af80-969b39f8c262
- 387eedc6-12e9-3b32-9881-63b6b5e85317
- c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180

Ожидаемый результат: вывод в терминале строки "Result for <номер ключа>: OK" для каждого из перечисленных вариантов

Невалидные ключи:

- 18252235-78e0-44a5-8720-556f0c7da17a
- e66075b6-ddad-445e-baf6-161b3289522b
- b6d53250-f07e-4352-a293-6102ddf7f1ca
- c2bc778a-1cb9-46c6-b435-0489649d2a42
- 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1

Ожидаемый результат: вывод в терминале строки "Result for <номер ключа>: FAIL" для каждого из перечисленных вариантов

Тестирование производилось в следующем окружении:
* ОС: Windows 10 pro x64
* openjdk version "11.0.7" 2020-04-14
* git version 2.26.0.windows.1