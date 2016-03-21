---
layout: default
title: Метод Account.GetActiveOffers
permalink: account/getActiveOffers/
comments: true
---
# Метод Account.GetActiveOffers
Возвращает список активных рекламных предложений (офферов), выполнив которые пользователь сможет получить соответствующее количество голосов на свой счёт внутри приложения.

Страница документации ВКонтакте [account.getActiveOffers](https://vk.com/dev/account.getActiveOffers).

## Синтаксис
``` csharp
public InformationAboutOffers GetActiveOffers(ulong? offset = null, ulong? count = null)
```

## Параметры
+ **offset** - Смещение, необходимое для выборки определенного подмножества офферов. положительное число, по умолчанию 0
+ **count** - Количество офферов, которое необходимо получить положительное число, по умолчанию 100, максимальное значение 100

## Результат
Возвращает массив, состоящий из общего количества старгетированных на текущего пользователя специальных предложений (первый элемент), и списка объектов с информацией о предложениях. 
В случае, если на пользователя не старгетировано ни одного специального предложения, массив будет содержать элемент 0 (количество специальных предложений).

## Пример
``` csharp
var offers = GetActiveOffers();
```

## Версия Вконтакте API v.5.45
Дата обновления: 10.02.2016 13:55:10