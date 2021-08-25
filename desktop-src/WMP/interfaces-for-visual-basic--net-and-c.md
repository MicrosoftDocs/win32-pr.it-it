---
title: Interfacce per Visual Basic .NET e C
description: Interfacce per Visual Basic .NET e C\
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Windows Media Player, interfacce
- Windows Media Player Dispositivi mobili, interfacce
- Windows Media Player a oggetti, interfacce
- modello a oggetti,interfacce
- ActiveX, interfacce
- Windows Media Player ActiveX, interfacce
- Windows Media Player controllo ActiveX per dispositivi mobili,interfacce
- informazioni di riferimento per il modello a oggetti, interfacce
- Informazioni di riferimento sul modello a oggetti dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7024c60235b0a545463826fc8948adf3716c9c2d5b491414212d788087404b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862581"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfacce per Visual Basic .NET e C #

Questa sezione documenta le interfacce esposte dal Windows Media Player ActiveX controllo .

Per recuperare interfacce specifiche vengono usati diversi metodi e proprietà dell'oggetto [AxWindowsMediaPlayer.](axwindowsmediaplayer-object--vb-and-c.md) Queste interfacce, a loro volta, possono avere proprietà e metodi delle funzioni di accesso per il recupero di altre interfacce.

Il Windows Media Player espone le interfacce seguenti.



| Interfaccia                                                      | Descrizione                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Accede a un CD o DVD in un'unità.                                                                                                                                  |
| [IWMPCdromCombo](iwmpcdromburn--vb-and-c.md)                   | Fornisce proprietà e metodi per gestire la creazione di CD audio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Accede a una raccolta di unità CD o DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Fornisce proprietà e metodi per gestire la copia o *lo scheggiamento* di tracce da un CD audio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Consente di includere sottotitoli in un file multimediale digitale.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Fornisce proprietà e metodi aggiuntivi per i sottotitoli codificati.                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Rappresenta i controlli di trasporto Windows Media Player, ad esempio Riproduci, Arresta e Sospendi.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Fornisce un metodo di controllo aggiuntivo per bloccare la riproduzione sul frame successivo o precedente.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Fornisce proprietà e metodi di controllo aggiuntivi per la selezione e il supporto della lingua audio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Fornisce proprietà e metodi per l'utilizzo di DVD.                                                                                                            |
| [Errore IWMP](iwmperror--vb-and-c.md)                           | Accede a una raccolta di [interfacce IWMPErrorItem](iwmperroritem--vb-and-c.md) per il recupero delle informazioni sugli errori.                                                |
| [Elemento IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Fornisce l'accesso alle informazioni sull'errore.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Fornisce una proprietà aggiuntiva dell'elemento di errore per ottenere un codice di condizione di errore.                                                                                   |
| **IWMPFolderMonitorServices**                                  | Non supportato per la programmazione .NET.                                                                                                                               |
| [Libreria IWMP](iwmplibrary--vb-and-c.md)                       | Rappresenta una libreria.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Fornisce metodi per enumerare le librerie.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | Non supportato per la programmazione .NET.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Consente di impostare e recuperare le proprietà di un elemento multimediale.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Fornisce l'accesso a una proprietà aggiuntiva dell'elemento multimediale.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Fornisce metodi aggiuntivi per accedere alle proprietà di un elemento multimediale.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Fornisce metodi che possono essere utilizzati per organizzare un'ampia raccolta di elementi multimediali.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Fornisce metodi che integrano **l'interfaccia IWMPMediaCollection.**                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Fornisce proprietà per ottenere informazioni sull'immagine contenuta in un file multimediale digitale rappresentato da un attributo di metadati **WM/Picture.**         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Fornisce proprietà per ottenere informazioni sugli attributi di metadati testuali complessi.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Fornisce proprietà e metodi per accedere alle statistiche relative alla qualità di una connessione di rete e per specificare e recuperare le impostazioni del proxy di rete.     |
| **IWMPPlayerApplication**                                      | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Non supportato per la programmazione .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Fornisce proprietà e metodi per organizzare, gestire e modificare elementi multimediali in una playlist.                                                                    |
| [Oggetto IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Accede a una raccolta di [interfacce IWMPPlaylist](iwmpplaylist--vb-and-c.md) in base al numero di indice.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Fornisce metodi per la modifica [delle interfacce IWMPPlaylist](iwmpplaylist--vb-and-c.md) e [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) in una raccolta. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Rappresenta una query composta.                                                                                                                                      |
| [Impostazioni IWMP](iwmpsettings--vb-and-c.md)                     | Fornisce proprietà e metodi che ottengono o impostano i valori Windows Media Player impostazioni.                                                                      |
| [Impostazioni IWMP2](iwmpsettings2--vb-and-c.md)                   | Fornisce proprietà e un metodo che integrano **l'interfaccia IWMPSettings.**                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Fornisce una proprietà e un metodo per accedere a una raccolta di stringhe in base al numero di indice.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Fornisce metodi che integrano **l'interfaccia IWMPStringCollection.**                                                                                          |
| **IWMPSyncDevice**                                             | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Non supportato per la programmazione .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | Non supportato per la programmazione .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti Visual Basic .NET e C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




