---
title: Uso di un callback di eventi per gestire la riproduzione memorizzata nel buffer
description: Uso di un callback di eventi per gestire la riproduzione memorizzata nel buffer
ms.assetid: 3b60daea-574d-430b-b14e-1fefceb69dfb
keywords:
- MidI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- MIDI (Musical Instrument Digital Interface), riproduzione memorizzata nel buffer
- riproduzione di file MIDI, riproduzione memorizzata nel buffer
- riproduzione memorizzata nel buffer
- Funzione CreateEvent
- MIDI (Musical Instrument Digital Interface), callback di eventi
- MIDI (Musical Instrument Digital Interface),callback di eventi
- riproduzione di file MIDI, callback di eventi
- callback di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747652c10471662daacfe433a8fc22d5248bf2fe2365b6b314e76d0b91ced127
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370267"
---
# <a name="using-an-event-callback-to-manage-buffered-playback"></a>Uso di un callback di eventi per gestire la riproduzione memorizzata nel buffer

Per usare un callback di evento, usare [la funzione CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) per recuperare l'handle di un evento. In una chiamata alla [**funzione midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) specificare CALLBACK \_ EVENT per il parametro *dwFlags.* Dopo aver utilizzato la funzione [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) ma prima di inviare eventi MIDI al dispositivo, creare un evento non associato chiamando la funzione [ResetEvent,](/windows/win32/api/synchapi/nf-synchapi-resetevent) specificando l'handle dell'evento recuperato **da CreateEvent**. Quindi, all'interno di un ciclo che controlla se il bit MHDR DONE è impostato nel membro \_ **dwFlags** della struttura [**MIDIHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) usare la funzione [WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) specificando l'handle dell'evento e un valore di timeout infinite come parametri.

Un callback di evento viene impostato da qualsiasi elemento che potrebbe causare un callback di funzione.

Poiché i callback degli eventi non ricevono notifiche specifiche di chiusura, fine o apertura, un'applicazione potrebbe dover controllare lo stato del processo che è in attesa dopo che si verifica l'evento. È possibile che una serie di attività possa essere completata al termine di **WaitForSingleObject.**

 

 