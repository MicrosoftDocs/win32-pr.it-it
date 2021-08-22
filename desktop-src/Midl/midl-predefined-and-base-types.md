---
title: Tipi di base e predefiniti MIDL
description: MIDL supporta i tipi di base e predefiniti seguenti.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- tipi di dati MIDL, predefiniti e di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ecbc76b3f680f0fffbabcff38e8562475e26be8ae4ac583a78c614d1651151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067081"
---
# <a name="midl-predefined-and-base-types"></a>Tipi di base e predefiniti MIDL

MIDL supporta i tipi di base e predefiniti seguenti.



| Tipo di dati                                  | Descrizione                                                                                                                                                                                             | Segno predefinito     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**Boolean**](boolean.md)                 | 8 bit. Non compatibile con [**le interfacce oleautomation;**](oleautomation.md) In alternativa, usare VARIANT \_ BOOL.                                                                                               | Senza segno         |
| [**byte**](byte.md)                       | 8 bit.                                                                                                                                                                                                 | (non applicabile) |
| [**Char**](char-idl.md)                   | 8 bit.                                                                                                                                                                                                 | Senza segno         |
| [**Doppia**](double.md)                   | Numero a virgola mobile a 64 bit.                                                                                                                                                                           | (non applicabile) |
| [**error \_ status \_ t**](error-status-t.md) | Intero senza segno a 32 bit per la restituzione di valori di stato per la gestione degli errori.                                                                                                                                 | Senza segno         |
| [**Galleggiante**](float.md)                     | Numero a virgola mobile a 32 bit.                                                                                                                                                                           | (non applicabile) |
| [**handle \_ t**](handle-t.md)              | Tipo di handle primitivo per l'associazione.                                                                                                                                                                      | (non applicabile) |
| [**hyper**](hyper.md)                     | Intero a 64 bit.                                                                                                                                                                                         | Firmato           |
| [**int**](int.md)                         | Intero a 32 bit. Nelle piattaforme a 16 bit, non può essere visualizzato nelle funzioni remote senza un qualificatore di dimensione, ad esempio [**short,**](short.md) [**small,**](small.md) [**long**](long.md) o [**hyper.**](hyper.md) | Firmato           |
| **\_\_int8**                               | Intero a 8 bit. Equivale a **piccolo**.                                                                                                                                                                 | Firmato           |
| **\_\_int16**                              | Intero a 16 bit. Equivale a **short**.                                                                                                                                                                | Firmato           |
| **\_\_int32**                              | Intero a 32 bit. Equivale a [**long.**](long.md)                                                                                                                                                     | Firmato           |
| [**\_\_int3264**](--int3264.md)           | Intero a 32 bit su piattaforme a 32 bit e a 64 bit nelle piattaforme a 64 bit.                                                                                                                       | Firmato           |
| [**\_\_int64**](--int64.md)               | Intero a 64 bit. Equivalente a [**hyper**](hyper.md).                                                                                                                                                   | Firmato           |
| [**long**](long.md)                       | Intero a 32 bit.                                                                                                                                                                                         | Firmato           |
| [**short**](short.md)                     | Intero da 16 bt.                                                                                                                                                                                          | Firmato           |
| [**Piccolo**](small.md)                     | Intero a 8 bit.                                                                                                                                                                                          | Firmato           |
| [**void**](void.md)                       | Indica che la routine non restituisce un valore.                                                                                                                                                   | (non applicabile) |
| **Vuoto \***                                | Puntatore a 32 bit solo per handle di contesto.                                                                                                                                                                | (non applicabile) |
| [**wchar \_ t**](wchar-t.md)                | Tipo predefinito a 16 bit per i caratteri wide.                                                                                                                                                             | Senza segno         |



 

 

 




