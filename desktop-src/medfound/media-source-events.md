---
description: Eventi di origine dei supporti
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventi di origine dei supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320781"
---
# <a name="media-source-events"></a>Eventi di origine dei supporti

Questo argomento elenca gli eventi inviati da origini multimediali e flussi multimediali. Le origini supporto possono anche inviare eventi personalizzati non elencati qui.

## <a name="media-source-events"></a>Eventi di origine dei supporti



| Event                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Evento MEEndOfPresentation](meendofpresentation.md)                       | Presentazione terminata. Tutti i flussi nella presentazione hanno raggiunto la fine del flusso.      |
| [Evento MENewStream](menewstream.md)                                       | È stato creato un nuovo flusso. L'evento contiene un puntatore al flusso.                            |
| [Evento MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) | Le caratteristiche dell'origine sono state modificate. Facoltativo.                                      |
| [Evento MESourceMetadataChanged](mesourcemetadatachanged.md)               | I metadati dell'origine sono stati modificati. Facoltativo.                                                   |
| [Evento MESourcePaused](mesourcepaused.md)                                 | L'origine è stata sospesa. Non tutte le origini supportano la sospensione.                                          |
| [Evento MESourceRateChanged](mesourceratechanged.md)                       | La frequenza di riproduzione dell'origine è cambiata. (Facoltativo; si applica se l'origine supporta il controllo della frequenza). |
| [Evento MESourceRateChangeRequested](mesourceratechangerequested.md)       | L'origine richiede una nuova velocità di riproduzione. Facoltativo.                                        |
| [Evento MESourceSeeked](mesourceseeked.md)                                 | L'origine è stata ricercata. Non tutte le origini supportano la ricerca.                                          |
| [Evento MESourceStarted](mesourcestarted.md)                               | Origine avviata.                                                                          |
| [Evento MESourceStopped](mesourcestopped.md)                               | Origine arrestata.                                                                          |
| [Evento MEUpdatedStream](meupdatedstream.md)                               | Un flusso esistente è stato cercato o riavviato. L'evento contiene un puntatore al flusso.         |



 

## <a name="media-stream-events"></a>Eventi del flusso multimediale



| Event                                                    | Descrizione                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Evento MEEndOfStream](meendofstream.md)                 | Il flusso è terminato.                                                                                                              |
| [Evento MEError](meerror.md)                             | Si è verificato un errore durante il flusso. Utilizzare questo evento per gli errori non correlati ad altri eventi elencati di seguito. |
| [Evento MEMediaSample](memediasample.md)                 | Il flusso ha generato un nuovo esempio.                                                                                         |
| [Evento MEStreamFormatChanged](mestreamformatchanged.md) | Il tipo di supporto è stato modificato. Facoltativo.                                                                                        |
| [Evento MEStreamPaused](mestreampaused.md)               | Il flusso è stato sospeso.                                                                                                         |
| [Evento MEStreamSeeked](mestreamseeked.md)               | Il flusso è stato cercato.                                                                                                         |
| [Evento MEStreamStarted](mestreamstarted.md)             | Il flusso è stato avviato.                                                                                                        |
| [Evento MEStreamStopped](mestreamstopped.md)             | Il flusso è stato interrotto.                                                                                                        |
| [Evento MEStreamThinMode](mestreamthinmode.md)           | La modalità di assottigliamento è stata avviata o arrestata. Facoltativo.                                                                              |
| [Evento MEStreamTick](mestreamtick.md)                   | Si è verificato un gap nel flusso. Facoltativo.                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Origini supporti](media-sources.md)
</dt> </dl>

 

 



