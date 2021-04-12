---
title: Mappe patch
description: Mappe patch
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- MIDI (Musical Instrument Digital Interface), Mapper MIDI
- MIDI (Musical Instrument Digital Interface), MIDI Mapper
- Mapper MIDI, mappe patch
- Mappe patch
- Programmi MIDI-modificare i messaggi
- Messaggi del controller del volume MIDI
- messaggi di modifica programma
- messaggi del controller del volume
- Mapper MIDI, messaggi di modifica del programma
- Mapper MIDI, messaggi del controller del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e418b0616d9ba9d2c2bcd05ebcb312ba0176ef5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329620"
---
# <a name="patch-maps"></a>Mappe patch

A ogni voce della mappa del canale può essere associata una mappa patch. Le mappe delle patch influiscono sul programma MIDI, sulla modifica e sui messaggi del controller del volume. Messaggi di modifica del programma indicano a un sintetizzatore di modificare il suono dello strumento (patch) per un canale specificato. I messaggi del controller del volume impostano il volume per un canale.

Una mappa di patch include una tabella di traduzione con una voce per ogni valore di modifica del programma 128. Ogni mappa di patch specifica quanto segue:

-   Valore di modifica di un programma di destinazione.
-   Volume scalare. Per ulteriori informazioni, vedere [volume Scalar](the-volume-scalar.md).
-   Mappa delle chiavi facoltativa. Per ulteriori informazioni, vedere la pagina relativa ai [mapping delle chiavi](key-maps.md).

Quando i messaggi di modifica del programma vengono ricevuti dal mapper MIDI, il valore di modifica del programma di destinazione viene sostituito con il valore di modifica del programma nel messaggio. Ad esempio, se il valore del programma di destinazione-modifica valore per programma-modifica 16 è 18, il mapper del MIDI modifica il messaggio di modifica del programma MIDI, come illustrato nella figura seguente.

![immagine del mapper MIDI](images/mmap-a03.gif)

 

 




