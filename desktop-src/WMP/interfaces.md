---
title: Interfacce WMP SDK
description: Interfacce WMP SDK
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
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
ms.openlocfilehash: ffff5a4c609d13d84972989ac32dae1600f5f02d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400074"
---
# <a name="wmp-sdk-interfaces"></a>Interfacce WMP SDK

In questa sezione vengono documentate le interfacce COM esposte dal controllo ActiveX Windows Media Player e dal controllo ActiveX Windows Media Player mobile.

I metodi delle funzioni di accesso dell'interfaccia **IWMPCore** o **IWMPPlayer** vengono utilizzati per recuperare interfacce specifiche. Queste interfacce, a loro volta, possono avere metodi della funzione di accesso per il recupero di interfacce aggiuntive. La chiamata a **QueryInterface** su una di queste interfacce è necessaria solo quando si recupera la versione di base di un'interfaccia e si desidera chiamare un metodo in una versione successiva della stessa interfaccia.

> [!Note]  
> Tutti i metodi e gli eventi sono completamente supportati in Windows Media Player 10 mobile e versioni successive, se non diversamente specificato in modo esplicito.

Il controllo Windows Media Player espone le interfacce seguenti.

| Interfaccia                                                    | Descrizione                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | Fornisce eventi originati dal controllo Media Player Windows a cui un programma di incorporamento può rispondere.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Accede a un CD o DVD in un'unità.                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Fornisce metodi per la gestione della creazione di CD audio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Accede a una raccolta di unità CD o DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Fornisce i metodi per gestire la copia delle tracce da un CD audio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Include didascalie con una clip multimediale.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Fornisce metodi di didascalia aggiuntivi.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Rappresenta i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Fornisce metodi di controllo aggiuntivi.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Fornisce metodi di controllo aggiuntivi.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera i puntatori ad altre interfacce e accede alle funzionalità di base del controllo. Si tratta dell'interfaccia radice per il modello a oggetti di Windows Media Player.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Fornisce metodi di base aggiuntivi.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Fornisce metodi di base aggiuntivi.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Accede al menu contenuto di un DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Accede a una raccolta di puntatori [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Fornisce informazioni sugli errori.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Fornisce metodi aggiuntivi per gli elementi error.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Espone gli eventi che provengono dal controllo Media Player Windows a cui un programma di incorporamento può rispondere.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Espone gli eventi che hanno origine dal controllo Windows Media Player 10 a cui un programma di incorporamento può rispondere. Questi eventi vengono usati in modo specifico per i programmi di sincronizzazione dei dispositivi. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Fornisce eventi correlati a ripping di CD, masterizzazione di CD, monitoraggio di cartelle e servizi di libreria remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Fornisce metodi per enumerare, analizzare e modificare le cartelle di file che Windows Media Player monitora per il contenuto multimediale digitale.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Gestisce il grafo DirectShow.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Rappresenta una libreria.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Fornisce metodi per enumerare le librerie.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Fornisce metodi per gestire la condivisione di librerie.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Imposta e recupera le proprietà di un elemento multimediale.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Fornisce metodi aggiuntivi per impostare e recuperare le proprietà di un elemento multimediale.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Fornisce metodi aggiuntivi per impostare e recuperare le proprietà di un elemento multimediale.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Accede a una raccolta di puntatori [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) .                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Fornisce metodi che integrano l'interfaccia **IWMPMediaCollection** .                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Recupera le informazioni sull'attributo dei metadati **WM/Picture** .                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Recupera informazioni sugli attributi di metadati testuali complessi.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Imposta e recupera le proprietà della connessione di rete utilizzata da Windows Media Player.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Controlla il comportamento dell'interfaccia utente del controllo Media Player di Windows.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Fornisce metodi aggiuntivi per il controllo di Windows Media Player.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Fornisce metodi aggiuntivi per il controllo di Windows Media Player.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Fornisce metodi aggiuntivi per il controllo di Windows Media Player.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Passa tra un controllo Media Player di Windows remoto e la modalità completa del lettore. Progettato per l'utilizzo da parte di programmi C++ che incorporano il controllo in modalità remota.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Utilizzato dall'host di un controllo remoto per modificare la modalità completa di Windows Media Player. Progettato per l'utilizzo con C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Imposta la priorità di elaborazione in background.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Crea e gestisce le playlist.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Accede a una raccolta di puntatori [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) in base al numero di indice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Modifica i puntatori [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) e [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Rappresenta una query composta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Fornisce servizi a Windows Media Player da un programma che ospita il controllo lettore. Progettato per l'utilizzo con C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Fornisce metodi per specificare o recuperare un valore che indica se la riproduzione viene eseguita solo nel processo corrente.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Imposta o recupera le impostazioni di Windows Media Player.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Imposta o recupera le impostazioni di Windows Media Player.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Specifica l'interfaccia utilizzata con Windows Media Player.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Accede a una raccolta di stringhe.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Fornisce metodi che integrano l'interfaccia **IWMPStringCollection** .                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Rappresenta un dispositivo in grado di sincronizzare i file multimediali digitali con Windows Media Player 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Fornisce un metodo che integra l'interfaccia **IWMPSyncDevice** .                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera i dispositivi disponibili che possono sincronizzare i file multimediali digitali con Windows Media Player 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Fornisce un metodo implementato dai filtri di origine DirectShow per gestire la modifica del formato dei file multimediali digitali.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Fornisce un metodo che configura il renderer video migliorato utilizzato da Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento del modello a oggetti per C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




