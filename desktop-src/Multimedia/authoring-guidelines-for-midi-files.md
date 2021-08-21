---
title: Linee guida per la creazione di file MIDI
description: Linee guida per la creazione di file MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- Instrument Digital Interface (MIDI), linee guida per la creazione di file
- MIDI (Instrument Digital Interface), linee guida per la creazione di file
- creazione di file MIDI, linee guida per la creazione di file
- assegnazioni di patch MIDI standard
- assegnazioni di chiavi MIDI standard
- Instrument Digital Interface (MIDI), assegnazioni di patch standard
- MIDI (Instrument Digital Interface), assegnazioni di patch standard
- Instrument Digital Interface (MIDI), assegnazioni di chiavi standard
- MIDI (Instrument Digital Interface), assegnazioni di chiavi standard
- creazione di file MIDI, assegnazioni di patch standard
- creazione di file MIDI, assegnazioni di chiavi standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe148c2fe1bb562aad994608a8c87c35e84bccb7d63ba1bc3ee3e5dd3bbc56a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065641"
---
# <a name="authoring-guidelines-for-midi-files"></a>Linee guida per la creazione di file MIDI

Seguire queste linee guida per creare file MIDI indipendenti dal dispositivo per Windows:

-   Usare le [assegnazioni di patch MIDI standard e](standard-midi-patch-assignments.md) [le assegnazioni di chiavi MIDI standard](standard-midi-key-assignments.md).
-   Inviare sempre un messaggio di modifica del programma a un canale per selezionare una patch prima di inviare altri messaggi a tale canale. Per i due canali ( 10 e 16) selezionare il numero di programma 0.
-   Seguire sempre un messaggio di modifica del programma MIDI con un messaggio del controller del volume principale MIDI (numero di controller 7) per impostare il volume relativo della patch.
-   Usare il valore 80 (0x50) per il controller di volume principale per i livelli di ascolto normali. Per livelli più bassi o più alti, è possibile usare valori inferiori o superiori.
-   Usare solo i messaggi MIDI seguenti: note-on with velocità, note-off, cambio di programma, pitch pitch, volume principale (controller 7) e dampermper (controller 64). I sintetizzatori interni sono necessari per rispondere a questi messaggi e la maggior parte degli strumenti midi risponde anche a tali messaggi.

 

 




