---
title: Invio System-Exclusive messaggi
description: Invio System-Exclusive messaggi
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- riproduzione di file MIDI, invio di messaggi
- invio di messaggi MIDI
- MidI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- MIDI (Musical Instrument Digital Interface), messaggi esclusivi del sistema
- riproduzione di file MIDI, messaggi esclusivi di sistema
- Messaggi MIDI esclusivi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad97371f56c042e5acd230aba6144f5f9734a594b370a791422b2e8f8148861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037261"
---
# <a name="sending-system-exclusive-messages"></a>Invio System-Exclusive messaggi

I messaggi midi esclusivi di sistema sono gli unici messaggi MIDI che non rientrano in un singolo valore doubleword. I messaggi esclusivi di sistema possono essere di qualsiasi lunghezza. Windows fornisce la [**funzione midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) per l'invio di messaggi esclusivi di sistema ai dispositivi di output MIDI. Per specificare blocchi di dati esclusivi del sistema MIDI, usare la [**struttura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

Dopo aver inviato un blocco di dati esclusivo del sistema usando **midiOutLongMsg,** è necessario attendere il completamento del driver di dispositivo con il blocco di dati prima di liberarlo. Se si inviano più blocchi di dati, è necessario monitorare il completamento di ogni blocco di dati in modo da sapere quando inviare blocchi aggiuntivi. Per informazioni sulle diverse tecniche per il monitoraggio del completamento dei blocchi di dati, vedere [Gestione dei blocchi di dati MIDI](managing-midi-data-blocks.md).

> [!Note]  
> Qualsiasi byte di stato MIDI diverso da un messaggio in tempo reale di sistema terminerà un messaggio esclusivo di sistema. Se si usano più blocchi di dati per inviare un singolo messaggio esclusivo di sistema, non inviare messaggi MIDI diversi da quelli in tempo reale tra blocchi di dati.

 

 

 