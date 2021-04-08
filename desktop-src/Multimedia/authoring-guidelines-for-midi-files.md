---
title: Linee guida per la creazione di file MIDI
description: Linee guida per la creazione di file MIDI
ms.assetid: 57e3d260-d275-4b0c-9db0-d036dd12fdb8
keywords:
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- MIDI (Musical Instrument Digital Interface), linee guida per la creazione di file
- creazione di file MIDI, linee guida per la creazione di file
- assegnazioni di patch MIDI standard
- assegnazioni di chiavi MIDI standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di patch standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di chiavi standard
- MIDI (Musical Instrument Digital Interface), assegnazioni di chiavi standard
- creazione di file MIDI, assegnazioni di patch standard
- creazione di file MIDI, assegnazioni di chiavi standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcfec1b5089fa3c58c18eb8990156df12db0ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045271"
---
# <a name="authoring-guidelines-for-midi-files"></a>Linee guida per la creazione di file MIDI

Per creare file MIDI indipendenti dal dispositivo per Windows, seguire queste linee guida:

-   Usare le [assegnazioni di patch MIDI standard](standard-midi-patch-assignments.md) e le [assegnazioni di chiavi MIDI standard](standard-midi-key-assignments.md).
-   Inviare sempre un messaggio di modifica del programma a un canale per selezionare una patch prima di inviare altri messaggi a tale canale. Per i due canali di percussione (10 e 16), selezionare programma numero 0.
-   Seguire sempre un messaggio di modifica del programma MIDI con un messaggio del controller principale del volume MIDI (controller numero 7) per impostare il volume relativo della patch.
-   Usare il valore 80 (0x50) per il controller principale del volume per i livelli di ascolto normali. Per i livelli più tranquilli o più forti, è possibile usare valori inferiori o superiori.
-   Usare solo i messaggi MIDI seguenti: note-on con velocità, nota-off, modifica del programma, curva di pitch, volume principale (controller 7) e pedale Damper (controller 64). I sintetizzatori interni sono necessari per rispondere a questi messaggi e la maggior parte degli strumenti musicali MIDI rispondono anche a tali messaggi.

 

 




