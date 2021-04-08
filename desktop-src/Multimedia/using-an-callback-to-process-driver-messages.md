---
title: Utilizzo di un callback di evento per elaborare i messaggi del driver
description: Utilizzo di un callback di evento per elaborare i messaggi del driver
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- audio Waveform, callback evento
- blocchi di dati audio, callback di evento
- audio Waveform, elaborazione dei messaggi del driver
- blocchi di dati audio, elaborazione dei messaggi del driver
- elaborazione dei messaggi del driver
- CreateEvent (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725415"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Utilizzo di un callback di evento per elaborare i messaggi del driver

Per usare un callback di evento, usare la funzione [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) per creare un evento di reimpostazione manuale. Nella chiamata alla funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) specificare l'evento di **callback \_** per il parametro *fdwOpen* . Dopo aver chiamato la funzione [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) , ma prima di inviare dati audio della forma d'onda al dispositivo, inserire l'evento in uno stato non segnalato chiamando la funzione [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) . Quindi, all'interno di un ciclo che controlla se il flag **WHDR \_ done** è impostato nel membro **dwFlags** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , chiamare la funzione [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) , specificando come parametri l'handle di evento e un valore di timeout.

Poiché i callback degli eventi non ricevono notifiche Close, done o Open specifiche, è possibile che un'applicazione debba controllare lo stato del processo in attesa dopo che si è verificato l'evento. È possibile che una serie di attività sia stata completata nel momento in cui [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) restituisce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Blocchi di dati audio](audio-data-blocks.md)
</dt> </dl>

 

 