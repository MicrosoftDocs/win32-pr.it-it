---
title: Invio di messaggi MIDI con buffer di flusso
description: Invio di messaggi MIDI con buffer di flusso
ms.assetid: f9e77637-098c-4ee8-bca9-a05ecce0c569
keywords:
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- riproduzione di file MIDI, buffer di flusso
- buffer di flusso, invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dbe2a2854abf9dd1ba67a93954c0823ac387b86
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725359"
---
# <a name="sending-midi-messages-with-stream-buffers"></a>Invio di messaggi MIDI con buffer di flusso

Quando l'applicazione funziona con i buffer di flusso, usa la funzione [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) per inviare tutti i messaggi MIDI (short e Long) al dispositivo. Per specificare i blocchi di dati di flusso, utilizzare le strutture [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) e [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . La struttura **MIDIHDR** contiene un indirizzo di un blocco di dati bloccato, la lunghezza del blocco di dati e alcuni flag assortiti. I dati vengono archiviati sotto forma di strutture **MIDIEVENT** . Il sistema impone un limite di dimensioni di 64K nei buffer di flusso.

Dopo aver usato **midiStreamOut** per inviare un buffer di flusso di dati, è necessario attendere che il driver di dispositivo non sia terminato con il blocco di dati prima di liberarlo. Se si inviano più blocchi di dati, è necessario monitorare il completamento di ogni blocco di dati in modo da stabilire quando inviare blocchi aggiuntivi. Per informazioni sulle diverse tecniche per il monitoraggio del completamento dei blocchi di dati, vedere [Managing MIDI Data](managing-midi-data-blocks.md)Blocks.

 

 