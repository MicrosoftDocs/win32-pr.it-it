---
title: Tipi di base e predefiniti di MIDL
description: MIDL supporta i tipi di base e predefiniti seguenti.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- tipi di dati MIDL, predefiniti e di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1afaa479969d65f162a9d57935aa7fbc539701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044598"
---
# <a name="midl-predefined-and-base-types"></a>Tipi di base e predefiniti di MIDL

MIDL supporta i tipi di base e predefiniti seguenti.



| Tipo di dati                                  | Descrizione                                                                                                                                                                                             | Segno predefinito     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**Boolean**](boolean.md)                 | 8 bit. Non compatibile con le interfacce [**oleautomation**](oleautomation.md) . usare invece la variante \_ bool.                                                                                               | Senza segno         |
| [**byte**](byte.md)                       | 8 bit.                                                                                                                                                                                                 | (non applicabile) |
| [**char**](char-idl.md)                   | 8 bit.                                                                                                                                                                                                 | Senza segno         |
| [**doppio**](double.md)                   | numero a virgola mobile a 64 bit.                                                                                                                                                                           | (non applicabile) |
| [**stato di errore \_ \_ t**](error-status-t.md) | Unsigned Integer a 32 bit per la restituzione di valori di stato per la gestione degli errori.                                                                                                                                 | Senza segno         |
| [**float**](float.md)                     | numero a virgola mobile a 32 bit.                                                                                                                                                                           | (non applicabile) |
| [**handle \_ t**](handle-t.md)              | Tipo di handle primitivo per l'associazione.                                                                                                                                                                      | (non applicabile) |
| [**Hyper**](hyper.md)                     | intero a 64 bit.                                                                                                                                                                                         | Firmato           |
| [**INT**](int.md)                         | intero a 32 bit. Nelle piattaforme a 16 bit non è possibile visualizzare le funzioni remote senza un qualificatore di dimensione, ad esempio [**short**](short.md), [**small**](small.md), [**Long**](long.md) o [**Hyper**](hyper.md). | Firmato           |
| **\_\_int8**                               | Integer a 8 bit. Equivalente a **small**.                                                                                                                                                                 | Firmato           |
| **\_\_Int16**                              | intero a 16 bit. Equivalente a **short**.                                                                                                                                                                | Firmato           |
| **\_\_Int32**                              | intero a 32 bit. Equivalente a [**Long**](long.md).                                                                                                                                                     | Firmato           |
| [**\_\_int3264**](--int3264.md)           | Intero a 32 bit su piattaforme a 32 bit e a 64 bit su piattaforme a 64 bit.                                                                                                                       | Firmato           |
| [**\_\_Int64**](--int64.md)               | intero a 64 bit. Equivalente a [**Hyper**](hyper.md).                                                                                                                                                   | Firmato           |
| [**long**](long.md)                       | intero a 32 bit.                                                                                                                                                                                         | Firmato           |
| [**short**](short.md)                     | intero a 16 BT.                                                                                                                                                                                          | Firmato           |
| [**piccolo**](small.md)                     | Integer a 8 bit.                                                                                                                                                                                          | Firmato           |
| [**void**](void.md)                       | Indica che la routine non restituisce un valore.                                                                                                                                                   | (non applicabile) |
| **vuoto \***                                | puntatore a 32 bit per solo handle di contesto.                                                                                                                                                                | (non applicabile) |
| [**WCHAR \_ t**](wchar-t.md)                | tipo predefinito a 16 bit per caratteri wide.                                                                                                                                                             | Senza segno         |



 

 

 




