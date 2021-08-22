---
title: Applicazione di patch Mappe
description: Applicazione di patch Mappe
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Instrument Digital Interface (MIDI), MIDI Mapper
- MIDI (Instrument Digital Interface), MIDI Mapper
- MIDI Mapper, mappe patch
- Mappe patch
- Messaggi di modifica del programma MIDI
- Messaggi midi del controller del volume
- messaggi di modifica del programma
- messaggi del controller del volume
- MIDI Mapper, messaggi di modifica del programma
- MIDI Mapper, messaggi volume-controller
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32f60ac486d7e8812b5cf71febe3794ae37d650bc795baa4c06ffb48ce5f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038266"
---
# <a name="patch-maps"></a>Applicazione di patch Mappe

A ogni voce della mappa dei canali può essere associata una mappa patch. Le mappe patch influiscono sui messaggi di modifica del programma MIDI e del controller del volume. I messaggi di modifica del programma indicano a un sintetizzatore di modificare il suono dello strumento (patch) per un canale specificato. I messaggi del controller del volume impostano il volume per un canale.

Una mappa patch include una tabella di conversione con una voce per ognuno dei 128 valori di modifica del programma. Ogni mappa patch specifica quanto segue:

-   Valore di modifica del programma di destinazione.
-   Scalare del volume. Per altre informazioni, vedere [Scalare del volume.](the-volume-scalar.md)
-   Mappa delle chiavi facoltativa. Per altre informazioni, vedere [Key Mappe](key-maps.md).

Quando il mapper MIDI riceve messaggi di modifica del programma, il valore di modifica del programma di destinazione viene sostituito con il valore di modifica del programma nel messaggio. Ad esempio, se il valore di modifica del programma di destinazione per la modifica del programma 16 è 18, il mapper MIDI modifica il messaggio di modifica del programma MIDI come illustrato nella figura seguente.

![immagine midi mapper](images/mmap-a03.gif)

 

 




