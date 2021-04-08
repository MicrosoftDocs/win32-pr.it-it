---
title: Invio di messaggi di System-Exclusive
description: Invio di messaggi di System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- MIDI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- riproduzione di file MIDI, messaggi esclusivi del sistema
- messaggi MIDI esclusivi del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872346"
---
# <a name="sending-system-exclusive-messages"></a>Invio di messaggi di System-Exclusive

MIDI System: i messaggi esclusivi sono gli unici messaggi MIDI che non rientrano in un singolo valore parola doppia. I messaggi esclusivi del sistema possono essere di qualsiasi lunghezza. Windows fornisce la funzione [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) per l'invio di messaggi esclusivi del sistema ai dispositivi di output MIDI. Per specificare i blocchi di dati esclusivi del sistema MIDI, utilizzare la struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

Dopo aver inviato un blocco di dati esclusivo del sistema tramite **midiOutLongMsg**, è necessario attendere il completamento del blocco di dati da parte del driver di dispositivo prima di liberarlo. Se si inviano più blocchi di dati, è necessario monitorare il completamento di ogni blocco di dati in modo da stabilire quando inviare blocchi aggiuntivi. Per informazioni sulle diverse tecniche per il monitoraggio del completamento dei blocchi di dati, vedere [Managing MIDI Data](managing-midi-data-blocks.md)Blocks.

> [!Note]  
> Qualsiasi byte di stato MIDI diverso da un messaggio di sistema in tempo reale terminerà un messaggio esclusivo del sistema. Se si usano più blocchi di dati per inviare un singolo messaggio esclusivo del sistema, non inviare messaggi MIDI diversi dai messaggi di sistema in tempo reale tra i blocchi di dati.

 

 

 