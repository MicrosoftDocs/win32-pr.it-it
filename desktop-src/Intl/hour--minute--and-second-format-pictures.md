---
description: Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale. Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Immagini in formato ora, minuto e secondo formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e201e72e4da621334a46f20c47e1dd5f731d7ea443bb9970ce07bb7f4e5455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130391"
---
# <a name="hour-minute-and-second-format-pictures"></a>Immagini in formato ora, minuto e secondo formato

Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale. Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.

> [!Note]  
> Nei tipi di formato le lettere "m", "s" e "t" devono essere minuscole e la lettera "h" deve essere minuscola per indicare l'orologio a 12 ore o maiuscolo ("H") per indicare l'orologio a 24 ore.

Le virgolette singole possono essere usate per contrassegnare i caratteri che devono essere visualizzati esattamente come specificato. Se l'applicazione deve visualizzare una virgoletta singola, deve inserire due virgolette singole in una riga. Ad esempio, "abc''bar", viene visualizzato come "abc'bar".

Nella tabella seguente vengono definiti i tipi di formato usati per rappresentare le ore.

| string | Significato                                                             |
|--------|---------------------------------------------------------------------|
| h      | Ore senza zeri iniziali per le ore a cifra singola (12 ore). |
| hh     | Ore con zeri iniziali per le ore a cifra singola (12 ore).    |
| H      | Ore senza zeri iniziali per le ore a cifra singola (24 ore). |
| HH     | Ore con zeri iniziali per le ore a cifra singola (24 ore).    |

Nella tabella seguente vengono definiti i tipi di formato usati per rappresentare i minuti.

| string | Significato                                                 |
|--------|---------------------------------------------------------|
| m      | Minuti senza zeri iniziali per minuti a cifra singola. |
| MM     | Minuti con zeri iniziali per minuti a cifra singola.    |

Nella tabella seguente vengono definiti i tipi di formato usati per rappresentare i secondi.

| string | Significato                                                 |
|--------|---------------------------------------------------------|
| s      | Secondi senza zeri iniziali per i secondi a cifra singola. |
| ss     | Secondi con zeri iniziali per secondi a cifra singola.    |

Nella tabella seguente vengono definiti i tipi di formato usati per rappresentare un indicatore di tempo.

| string | Significato|
| ---    | ---    |
| t      | Stringa del marcatore temporale di un carattere.<br />**Nota:** Questo formato non è consigliato per l'uso con determinate lingue, ad esempio il giapponese (Giappone). Con questo formato, un'applicazione accetta sempre il primo carattere della stringa del marcatore temporale, definito da [LOCALE_S1159](locale-s1159.md) (AM) e [LOCALE_S2359](locale-s2359.md) (PM). Per questo scopo, l'applicazione può creare una formattazione non corretta con la stessa stringa usata sia per AM che per PM.|
| tt     | Stringa marcatore temporale a più caratteri. |
