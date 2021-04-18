---
description: Eventi della sessione multimediale
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Eventi della sessione multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e128fc5e11f70fe47d02356ce44629b98bfdfe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320704"
---
# <a name="media-session-events"></a>Eventi della sessione multimediale

La maggior parte delle operazioni della sessione multimediale viene eseguita in modo asincrono, pertanto l'applicazione deve restare in ascolto degli eventi usando l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) della sessione multimediale. (L'interfaccia [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) eredita **IMFMediaEventGenerator**). La sequenza esatta di eventi dipende dall'applicazione, ma gli eventi seguenti vengono generati dalla sessione multimediale in quasi tutte le situazioni.



| Event                                                                  | Descrizione                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Generato quando l'origine del supporto ha completato la presentazione. È possibile che i dati vengano ancora spostati nella pipeline in questo momento.                                                                                                     |
| [MEError](meerror.md)                                                 | Generato se si verifica un errore durante il flusso.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Generato quando il metodo [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) viene completato. Questo è l'ultimo evento accodato dalla sessione multimediale. Dopo aver ricevuto questo evento, è possibile arrestare tutte le origini multimediali create. |
| [MESessionEnded](mesessionended.md)                                   | Generato quando la sessione multimediale viene eseguita con l'ultima presentazione.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Notifica all'applicazione l'ora di presentazione quando la nuova presentazione viene avviata.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Generato quando il metodo [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) viene completato. A meno che non si sia verificato un errore, in questo momento i dati passano attraverso la pipeline.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Generato quando il metodo di [**topologia**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completato. A meno che non si verifichi un errore, l'applicazione non deve eseguire alcuna azione.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Generato in momenti diversi quando lo stato di una topologia cambia.                                                                                                                                                                 |



 

Il metodo [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) non genera un evento. Il metodo **Shutdown** è sincrono. Quando il metodo restituisce un risultato, è possibile rilasciare il puntatore al callback di evento.

Oltre agli eventi della sessione multimediale, l'applicazione potrebbe ricevere eventi dai sink di supporto nella topologia. Possono essere eventi personalizzati definiti dal sink multimediale, che potrebbero contenere dati arbitrari. Ad esempio, il sink potrebbe derivare i dati dell'evento dai dati di origine, che possono provenire da un'origine esterna non attendibile. Un'applicazione deve ignorare tutti gli eventi che non riconosce e prestare attenzione durante l'analisi dei dati degli eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> </dl>

 

 



