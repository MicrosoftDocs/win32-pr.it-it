---
title: Uso di un callback di eventi per elaborare i messaggi dei driver
description: Uso di un callback di eventi per elaborare i messaggi dei driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio waveform, callback di eventi
- blocchi di dati audio, callback di eventi
- audio waveform, elaborazione di messaggi del driver
- blocchi di dati audio, elaborazione di messaggi del driver
- elaborazione di messaggi del driver
- Funzione CreateEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5bdbfe46fed9fa9124a031e90af3bfefb983caf6743415d90c645afc42c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801201"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Uso di un callback di eventi per elaborare i messaggi dei driver

Per usare un callback di evento, usare [**la funzione CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) per creare un evento di reimpostazione manuale. Nella chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) specificare **CALLBACK \_ EVENT** per il *parametro fdwOpen.* Dopo aver chiamato la funzione [**waveOutPrepareHeader,**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) ma prima di inviare dati audio waveform al dispositivo, impostare l'evento su uno stato non associato chiamando la [**funzione ResetEvent.**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) Quindi, all'interno di un ciclo che controlla se il flag **WHDR \_ DONE** è impostato nel membro **dwFlags** della struttura [**WAVEHDR,**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) chiamare la funzione [WaitForSingleObject,](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) specificando come parametri l'handle dell'evento e un valore di timeout.

Poiché i callback degli eventi non ricevono notifiche specifiche di chiusura, fine o apertura, un'applicazione potrebbe dover controllare lo stato del processo che è in attesa dopo che si verifica l'evento. È possibile che alcune attività siano state completate entro il momento in cui [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) viene restituito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blocchi di dati audio](audio-data-blocks.md)
</dt> </dl>

 

 