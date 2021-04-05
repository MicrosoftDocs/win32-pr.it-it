---
title: Utilizzo di un callback di evento per gestire la riproduzione memorizzata nel buffer
description: Utilizzo di un callback di evento per gestire la riproduzione memorizzata nel buffer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- CreateEvent (funzione)
- MIDI (Musical Instrument Digital Interface), callback di evento
- MIDI (Musical Instrument Digital Interface), callback di evento
- riproduzione di file MIDI, callback di evento
- callback evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6f6cc7bec7971c117cb81b2f823d7184bc2fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725418"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Utilizzo di un callback di evento per gestire la riproduzione memorizzata nel buffer

Per usare un callback di evento, usare la funzione [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) per recuperare l'handle di un evento. In una chiamata alla funzione [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) , specificare \_ l'evento di callback per il parametro *dwFlags* . Dopo aver usato la funzione [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) ma prima di inviare eventi MIDI al dispositivo, creare un evento non segnalato chiamando la funzione [ResetEvent](/windows/win32/api/synchapi/nf-synchapi-resetevent) , specificando l'handle di evento recuperato da **CreateEvent**. Quindi, all'interno di un ciclo che controlla se il \_ bit feerika Done è impostato nel membro **dwFlags** della struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) , usare la funzione [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , specificando l'handle di evento e un valore di timeout infinito come parametri.

Un callback di evento viene impostato da qualsiasi elemento che potrebbe causare un callback di funzione.

Poiché i callback degli eventi non ricevono notifiche Close, done o Open specifiche, è possibile che un'applicazione debba controllare lo stato del processo in attesa dopo che si è verificato l'evento. È possibile che un numero di attività possa essere completato dal momento in cui **WaitForSingleObject** restituisce.

 

 