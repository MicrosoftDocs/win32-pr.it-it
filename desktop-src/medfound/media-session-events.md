---
description: Eventi della sessione multimediale
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Eventi della sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffecb3f4e3f4b3a3b30be95fcc45adcb81c1a84dd04ed8cf637bad759512a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724011"
---
# <a name="media-session-events"></a>Eventi della sessione multimediale

La maggior parte delle operazioni della sessione multimediale viene eseguita in modo asincrono, quindi l'applicazione deve restare in ascolto degli eventi usando [**l'interfaccia IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale. [**L'interfaccia IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) eredita **IMFMediaEventGenerator.** La sequenza esatta di eventi dipenderà dall'applicazione, ma gli eventi seguenti vengono generati dalla sessione multimediale in quasi tutte le situazioni.



| Event                                                                  | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Generato quando l'origine multimediale ha completato la presentazione. I dati potrebbero essere ancora in movimento nella pipeline in questo momento.                                                                                                     |
| [ERRORE MEError](meerror.md)                                                 | Generato se si verifica un errore durante il flusso.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Generato al completamento del metodo [**Close.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) Questo è l'ultimo evento accodato dalla sessione multimediale. Dopo aver ricevuto questo evento, è possibile arrestare tutte le origini multimediali create. |
| [MESessionEnded](mesessionended.md)                                   | Generato quando la sessione multimediale viene completata con l'ultima presentazione.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Notifica all'applicazione l'ora di inizio della nuova presentazione.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Generato al completamento del metodo [**Start.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) A meno che non si sia verificato un errore, a questo punto i dati passano attraverso la pipeline.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Generato al [**completamento del metodo SetTopology.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) A meno che non si verifichi un errore, l'applicazione non deve eseguire alcuna azione.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Generato in momenti diversi quando cambia lo stato di una topologia.                                                                                                                                                                 |



 

Il [**metodo IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) non genera un evento . Il **metodo Shutdown** è sincrono. Al termine di questo metodo, è possibile rilasciare il puntatore di callback dell'evento.

Oltre agli eventi della sessione multimediale, l'applicazione potrebbe ricevere eventi dai sink multimediali nella topologia. Possono essere eventi personalizzati definiti dal sink multimediale, che possono contenere dati arbitrari. Ad esempio, il sink potrebbe derivare i dati dell'evento dai dati di origine, che possono derivare da un'origine esterna non attendibile. Un'applicazione deve ignorare tutti gli eventi che non riconosce e prestare attenzione durante l'analisi dei dati degli eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



