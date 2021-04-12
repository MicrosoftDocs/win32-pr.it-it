---
title: Gestione della registrazione MIDI
description: Gestione della registrazione MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- MIDI (Musical Instrument Digital Interface), registrazione
- MIDI (Musical Instrument Digital Interface), registrazione
- registrazione dell'audio MIDI, gestione
- Registrazione MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472774"
---
# <a name="managing-midi-recording"></a>Gestione della registrazione MIDI

Dopo aver aperto un dispositivo MIDI, è possibile iniziare a registrare i dati MIDI. Windows fornisce le funzioni seguenti per la gestione della registrazione MIDI.



| Valore                                      | Significato                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Invia un buffer al driver di dispositivo in modo che possa essere riempito con i dati MIDI esclusivi del sistema registrati. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Interrompe la registrazione MIDI e contrassegna tutti i buffer in sospeso come eseguito.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Avvia la registrazione MIDI e reimposta il timestamp su zero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Interrompe la registrazione MIDI.                                                                             |



 

Per inviare i buffer al driver di dispositivo per la registrazione di messaggi esclusivi del sistema, usare [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). L'applicazione riceve una notifica quando i buffer sono riempiti con dati registrati esclusivi del sistema. Per altre informazioni sulle tecniche di notifica, vedere [Managing MIDI Data blocks](managing-midi-data-blocks.md).

La funzione [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) avvia il processo di registrazione. Quando si registrano messaggi esclusivi del sistema, inviare almeno un buffer al driver prima di avviare la registrazione. Per arrestare la registrazione, usare [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Prima di chiudere il dispositivo usando la funzione [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , contrassegnare tutti i blocchi di dati in sospeso come vengono eseguiti chiamando [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Le applicazioni che richiedono dati timestamp utilizzano una funzione di callback per ricevere dati MIDI. Se i requisiti di temporizzazione non sono severi, è possibile usare un callback di finestra o di thread. Tuttavia, non è possibile usare un callback di evento per ricevere dati MIDI.

Per registrare messaggi esclusivi del sistema con applicazioni che non utilizzano buffer di flusso, è necessario fornire il driver di dispositivo con i buffer. Questi buffer vengono specificati usando una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 