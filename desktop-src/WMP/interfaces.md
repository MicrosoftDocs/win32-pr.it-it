---
title: Interfacce WMP SDK
description: Interfacce WMP SDK
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player,interfacce
- Windows Media Player Dispositivi mobili, interfacce
- Windows Media Player a oggetti, interfacce
- modello a oggetti,interfacce
- ActiveX, interfacce
- Windows Media Player ActiveX, interfacce
- Windows Media Player Controllo ActiveX per dispositivi mobili, interfacce
- informazioni di riferimento per il modello a oggetti, interfacce
- Informazioni di riferimento sul modello a oggetti dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123501"
---
# <a name="wmp-sdk-interfaces"></a>Interfacce WMP SDK

Questa sezione documenta le interfacce COM esposte dal controllo Windows Media Player ActiveX e dal controllo Windows Media Player Mobile ActiveX.

I metodi della funzione di accesso **dell'interfaccia IWMPCore** o **IWMPPlayer** vengono usati per recuperare interfacce specifiche. Queste interfacce, a loro volta, possono avere metodi di funzione di accesso per il recupero di altre interfacce. La **chiamata di QueryInterface** su una di queste interfacce è necessaria solo quando si recupera la versione di base di un'interfaccia e si vuole chiamare un metodo in una versione successiva della stessa interfaccia.

> [!Note]  
> Tutti i metodi e gli eventi sono completamente supportati in Windows Media Player 10 Mobile e versioni successive, a meno che non venga specificato diversamente in modo esplicito.

Il Windows Media Player controllo espone le interfacce seguenti.

| Interfaccia                                                    | Descrizione                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_Eventi WMPOCX](-wmpocxevents-interface.md)                | Fornisce eventi provenienti dal controllo Windows Media Player a cui un programma di incorporamento può rispondere.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Accede a un CD o DVD in un'unità.                                                                                                                                                          |
| [IWMPCdromNz](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Fornisce metodi per gestire la creazione di CD audio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Accede a una raccolta di unità CD o DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Fornisce metodi per gestire la copia di tracce da un CD audio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Include i sottotitoli con un clip multimediale.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Fornisce metodi di sottotitoli codificati aggiuntivi.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Rappresenta i controlli di trasporto Windows Media Player, ad esempio Play, Stop e Pause.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Fornisce metodi di controllo aggiuntivi.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Fornisce metodi di controllo aggiuntivi.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera puntatori ad altre interfacce e accede alle funzionalità di base del controllo. Si tratta dell'interfaccia radice per il modello Windows Media Player a oggetti.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Fornisce metodi di base aggiuntivi.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Fornisce metodi di base aggiuntivi.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Accede al menu del contenuto di un DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Accede a una raccolta di [puntatori IWMPErrorItem.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Fornisce informazioni sugli errori.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Fornisce metodi aggiuntivi per gli elementi di errore.                                                                                                                                                   |
| [Eventi IWMP](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Espone gli eventi che hanno origine dal controllo Windows Media Player a cui un programma di incorporamento può rispondere.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Espone gli eventi che hanno origine dal controllo Windows Media Player 10 a cui un programma di incorporamento può rispondere. Questi eventi vengono usati in modo specifico per i programmi di sincronizzazione dei dispositivi. |
| [Eventi IWMP3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Fornisce eventi correlati al ripping di CD, alla masterizzazione di CD, al monitoraggio delle cartelle e ai servizi di libreria remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Fornisce metodi per enumerare, analizzare e modificare le cartelle di file Windows Media Player monitora il contenuto multimediale digitale.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Gestisce il DirectShow grafico.                                                                                                                                                             |
| [Libreria IWMP](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Rappresenta una libreria.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Fornisce metodi per enumerare le librerie.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Fornisce metodi per gestire la condivisione di librerie.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Imposta e recupera le proprietà di un elemento multimediale.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Fornisce metodi aggiuntivi per impostare e recuperare le proprietà di un elemento multimediale.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Fornisce metodi aggiuntivi per impostare e recuperare le proprietà di un elemento multimediale.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Accede a una raccolta di [puntatori IWMPMedia.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Fornisce metodi che integrano **l'interfaccia IWMPMediaCollection.**                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Recupera informazioni sull'attributo **dei metadati WM/Picture.**                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Recupera informazioni sugli attributi di metadati testuali complessi.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Imposta e recupera le proprietà della connessione di rete usata da Windows Media Player.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Controlla il comportamento dell'interfaccia Windows Media Player utente del controllo.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Fornisce metodi aggiuntivi per il controllo Windows Media Player.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Fornisce metodi aggiuntivi per il controllo Windows Media Player.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Fornisce metodi aggiuntivi per il controllo Windows Media Player.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Passa da un controllo Windows Media Player remoto alla modalità completa del lettore. Progettato per l'uso da parte di programmi C++ che incorporano il controllo in modalità remota.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Utilizzato dall'host di un controllo remoto per modificare la modalità completa di Windows Media Player. Progettato per l'uso con C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Imposta la priorità di elaborazione in background.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Crea e gestisce playlist.                                                                                                                                                            |
| [Oggetto IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Accede a una raccolta di [puntatori IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) in base al numero di indice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Modifica i [puntatori IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) [e IWMPPlaylistArray.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Rappresenta una query composta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Fornisce servizi per Windows Media Player da un programma che ospita il controllo Player. Progettato per l'uso con C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Fornisce metodi per specificare o recuperare un valore che indica se la riproduzione avviene solo nel processo corrente.                                                                          |
| [Impostazioni IWMP](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Imposta o recupera Windows Media Player impostazioni.                                                                                                                                          |
| [Impostazioni IWMP2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Imposta o recupera Windows Media Player impostazioni.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Specifica l'interfaccia utilizzata con Windows Media Player.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Accede a una raccolta di stringhe.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Fornisce metodi che integrano **l'interfaccia IWMPStringCollection.**                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Rappresenta un dispositivo in grado di sincronizzare i file multimediali digitali con Windows Media Player 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Fornisce un metodo che integra **l'interfaccia IWMPSyncDevice.**                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera i dispositivi disponibili che possono sincronizzare i file multimediali digitali con Windows Media Player 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Fornisce un metodo implementato da DirectShow di origine per gestire la modifica del formato dei file multimediali digitali.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Fornisce un metodo che configura il renderer video avanzato usato da Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sul modello a oggetti per C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




