---
description: Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale. Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Immagini di formato ora, minuto e secondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058360"
---
# <a name="hour-minute-and-second-format-pictures"></a>Immagini di formato ora, minuto e secondo

Questo argomento descrive i tipi di formato per le stringhe usate per comporre l'immagine del formato per una stringa temporale. Ogni immagine di formato è costituita da una combinazione di una stringa di ognuno dei tipi di formato.

> [!Note]  
> Nei tipi di formato le lettere "m", "s" e "t" devono essere minuscole e la lettera "h" deve essere minuscola per indicare il formato a 12 ore o maiuscolo ("H") per indicare il formato a 24 ore.

È possibile utilizzare le virgolette singole per contrassegnare i caratteri che devono essere visualizzati esattamente come specificato. Se l'applicazione deve visualizzare una virgoletta singola, deve inserire due virgolette singole in una riga. Ad esempio,' ABC '' barra ' viene visualizzato come "abc'bar".

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare le ore.

| string | Significato                                                             |
|--------|---------------------------------------------------------------------|
| h      | Ore senza zeri iniziali per le ore a una sola cifra (orario a 12 ore). |
| hh     | Ore con zeri iniziali per le ore a una sola cifra (orario a 12 ore).    |
| H      | Ore senza zeri iniziali per le ore a una sola cifra (orario a 24 ore). |
| HH     | Ore con zeri iniziali per le ore a una sola cifra (orario a 24 ore).    |

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i minuti.

| string | Significato                                                 |
|--------|---------------------------------------------------------|
| m      | Minuti senza zeri iniziali per minuti a una sola cifra. |
| MM     | Minuti con zeri iniziali per minuti a una sola cifra.    |

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare i secondi.

| string | Significato                                                 |
|--------|---------------------------------------------------------|
| s      | Secondi senza zeri iniziali per i secondi a una sola cifra. |
| ss     | Secondi con zeri iniziali per i secondi a una sola cifra.    |

Nella tabella seguente vengono definiti i tipi di formato utilizzati per rappresentare un marcatore temporale.

| string | Significato|
| ---    | ---    |
| u      | Stringa del marcatore del tempo di un solo carattere.<br />**Nota:** Questo formato non è consigliato per l'uso con determinate lingue, ad esempio giapponese (Giappone). Con questo formato, un'applicazione accetta sempre il primo carattere dalla stringa del marcatore temporale, definito da [LOCALE_S1159](locale-s1159.md) (AM) e [LOCALE_S2359](locale-s2359.md) (PM). Per questo motivo, l'applicazione può creare una formattazione non corretta con la stessa stringa utilizzata sia per AM che per PM.|
| tt     | Stringa del marcatore del tempo multicarattere. |
