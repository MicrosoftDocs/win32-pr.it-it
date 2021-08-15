---
title: Linee guida per la creazione di file MIDI
description: Linee guida per la creazione di file MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- creazione di file MIDI, linee guida per la creazione di file
- assegnazioni di patch MIDI standard
- assegnazioni di tasti MIDI standard
- MidI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di tasti standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di tasti standard
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

-   Usare le [assegnazioni di patch MIDI](standard-midi-patch-assignments.md) standard e le assegnazioni di chiavi [MIDI standard](standard-midi-key-assignments.md).
-   Inviare sempre un messaggio di modifica del programma a un canale per selezionare una patch prima di inviare altri messaggi a tale canale. Per i due canali di arsiote (10 e 16), selezionare il programma numero 0.
-   Seguire sempre un messaggio di modifica del programma MIDI con un messaggio del controller del volume principale MIDI (numero controller 7) per impostare il volume relativo della patch.
-   Usare il valore 80 (0x50) per il controller del volume principale per i normali livelli di ascolto. Per livelli più bassi o più alti, è possibile usare valori inferiori o superiori.
-   Usare solo i messaggi MIDI seguenti: note-on con velocità, note-off, cambio programma, pitch curve, volume principale (controller 7) e acceleratore ammortizzatore (controller 64). I sintetizzatori interni sono necessari per rispondere a questi messaggi e anche la maggior parte degli strumenti musicali MIDI risponde a tali messaggi.

 

 




