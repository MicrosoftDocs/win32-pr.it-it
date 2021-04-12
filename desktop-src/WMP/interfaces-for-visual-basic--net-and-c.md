---
title: Interfacce per Visual Basic .NET e C
description: Interfacce per Visual Basic .NET e C \
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Windows Media Player, interfacce
- Windows Media Player Mobile, interfacce
- Modello a oggetti di Windows Media Player, interfacce
- modello a oggetti, interfacce
- Controllo ActiveX, interfacce
- Controllo ActiveX Windows Media Player, interfacce
- Controllo ActiveX Windows Media Player Mobile, interfacce
- riferimento per il modello a oggetti, le interfacce
- riferimento al modello a oggetti Interface
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a301cb075ccee049272f1db9b2582aeae6697fa3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221701"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfacce per Visual Basic .NET e C #

In questa sezione vengono documentate le interfacce esposte dal controllo ActiveX di Windows Media Player.

Per recuperare interfacce specifiche vengono usate diverse proprietà e metodi dell' [oggetto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) . Queste interfacce, a loro volta, possono avere proprietà e metodi della funzione di accesso per il recupero di interfacce aggiuntive.

Il controllo Windows Media Player espone le interfacce seguenti.



| Interfaccia                                                      | Descrizione                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Accede a un CD o DVD in un'unità.                                                                                                                                  |
| [IWMPCdromBurn](iwmpcdromburn--vb-and-c.md)                   | Fornisce proprietà e metodi per la gestione della creazione di CD audio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Accede a una raccolta di unità CD o DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Fornisce le proprietà e i metodi per gestire la copia, o l' *estrazione*, di tracce da un CD audio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Fornisce un modo per includere le didascalie con un file multimediale digitale.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Fornisce proprietà e metodi aggiuntivi per la didascalia.                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Rappresenta i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Fornisce un metodo di controllo aggiuntivo per bloccare la riproduzione nel frame successivo o precedente.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Fornisce proprietà e metodi di controllo aggiuntivi per la selezione e il supporto della lingua audio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Fornisce le proprietà e i metodi per l'utilizzo dei DVD.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Accede a una raccolta di interfacce [IWMPErrorItem](iwmperroritem--vb-and-c.md) per il recupero delle informazioni sull'errore.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Consente di accedere alle informazioni sull'errore.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Fornisce una proprietà dell'elemento di errore aggiuntiva per ottenere un codice di condizione di errore.                                                                                   |
| **IWMPFolderMonitorServices**                                  | Non supportato per la programmazione .NET.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Rappresenta una libreria.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Fornisce metodi per enumerare le librerie.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | Non supportato per la programmazione .NET.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Consente di impostare e recuperare le proprietà di un elemento multimediale.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Consente di accedere a una proprietà di elemento multimediale aggiuntiva.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Fornisce metodi aggiuntivi per accedere alle proprietà di un elemento multimediale.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Fornisce metodi che possono essere usati per organizzare un'ampia raccolta di elementi multimediali.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Fornisce metodi che integrano l'interfaccia **IWMPMediaCollection** .                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Fornisce le proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo di metadati **WM/Picture** .         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Fornisce le proprietà per ottenere informazioni sugli attributi di metadati testuali complessi.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Fornisce proprietà e metodi per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.     |
| **IWMPPlayerApplication**                                      | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Non supportato per la programmazione .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Fornisce proprietà e metodi per organizzare, gestire e modificare gli elementi multimediali in una playlist.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Accede a una raccolta di interfacce [IWMPPlaylist](iwmpplaylist--vb-and-c.md) in base al numero di indice.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Fornisce metodi per la modifica delle interfacce [IWMPPlaylist](iwmpplaylist--vb-and-c.md) e [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) in una raccolta. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Rappresenta una query composta.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Fornisce proprietà e metodi che ottengono o impostano i valori delle impostazioni di Windows Media Player.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Fornisce le proprietà e un metodo che integrano l'interfaccia **IWMPSettings** .                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Fornisce una proprietà e un metodo per accedere a una raccolta di stringhe in base al numero di indice.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Fornisce metodi che integrano l'interfaccia **IWMPStringCollection** .                                                                                          |
| **IWMPSyncDevice**                                             | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | Non supportato per la programmazione .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento del modello a oggetti per Visual Basic .NET e C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




