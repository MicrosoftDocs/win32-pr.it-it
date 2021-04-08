---
title: Panoramica di Download Manager
description: Panoramica di Download Manager
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player Online Stores, Download in tempo reale
- negozi online, Download in tempo reale
- digitare 2 negozi online, Download in tempo reale
- Windows Media Player Online Stores, Download in background
- negozi online, Download in background
- digitare 2 negozi online, Download in background
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
- Download in tempo reale
- Download in background
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045259"
---
# <a name="download-manager-overview"></a>Panoramica di Download Manager

Microsoft Windows Media Player fornisce riquadri attività di archivio online che contengono una finestra del browser ospitata. Tramite gli archivi online, gli utenti possono interagire con le pagine Web del negozio online tramite Internet.

Windows Media Player Download Manager fornisce un modello a oggetti che è possibile utilizzare per gestire le attività associate al download del contenuto nel computer dell'utente da Microsoft Internet Information Services (IIS) tramite Hypertext Transfer Protocol (HTTP). Con Download Manager è possibile:

-   Gestione simultanea di più download come raccolta.
-   Specificare un URL per un file e avviarlo scaricando tramite HTTP.
-   Eseguire una query per lo stato di download e lo stato di avanzamento.
-   Sospendere, riprendere o annullare un download.
-   Consente di specificare se un download viene eseguito in background o in tempo reale. Il download in background è disponibile solo nel sistema operativo Microsoft Windows XP. Vedere [informazioni sul download in background e in tempo reale](#about-background-and-real-time-downloading).
-   Consente di specificare la modalità di visualizzazione del contenuto nella libreria. Vedere [informazioni sull'integrazione della libreria](#about-library-integration).

Download Manager è la soluzione per scaricare il contenuto dal codice di script nelle pagine Web ospitate. Per scaricare il contenuto usando il codice C++, usare il Servizio trasferimento intelligente in background di Windows XP (BITS). Per ulteriori informazioni, vedere [bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Informazioni sul download in tempo reale e in background

Download Manager offre due tipi di download: background e in tempo reale. Il tipo usato dipende dall'utente ed è possibile consentire all'utente di selezionare anche il tipo di download. Se si sceglie di consentire all'utente di selezionare il tipo di download, assicurarsi di illustrare le differenze tra i due tipi disponibili.

Il download in tempo reale si verifica in una sola volta. Quando l'utente avvia un download di file, l'intero file viene trasferito al computer dell'utente in un unico flusso continuo. L'utente non è in grado di sospendere o interrompere il download. Se l'utente sceglie di chiudere Windows Media Player prima del completamento del download, perderà tutti i file incompleti ed è necessario scaricarli dall'inizio per acquisire il contenuto.

Il vantaggio principale del download in tempo reale è che consente all'utente di acquisire il contenuto più velocemente rispetto al download in background. Il download in tempo reale è disponibile per gli utenti di Windows XP, ma è l'unico tipo di download disponibile nelle versioni del sistema operativo Windows precedenti a Windows XP.

Il download in background avviene in modo a fasi. Quando l'utente avvia un download in background, le parti del file vengono trasferite nel computer dell'utente quando è disponibile il tempo del processore. È possibile sospendere e riprendere un download in background. Se l'utente sceglie di chiudere Windows Media Player prima del completamento del download dello sfondo, la condizione dei file incompleti viene salvata e il download può continuare in background, anche dopo il riavvio del computer.

Il download in background può richiedere più tempo del download in tempo reale, perché il processo di download si verifica solo quando il processore non sta eseguendo altre attività.

Il download in background è disponibile solo quando si utilizza Windows XP.

## <a name="about-library-integration"></a>Informazioni sull'integrazione della libreria

Windows Media Player può organizzare automaticamente il contenuto del negozio online nella libreria. Per abilitare questa impostazione, è necessario specificare un valore per l'attributo **WM/contentdistributor** per ogni file multimediale digitale. Quando un file multimediale digitale viene aggiunto alla libreria, che si verifica automaticamente quando si usa gestione download, il file viene elencato automaticamente nel nodo **musica acquistato** o **video acquistati** . Se, ad esempio, il valore per **WM/contentdistributor** è "Proseware" e il file multimediale digitale contiene musica, il contenuto verrà visualizzato nella libreria nel percorso seguente:

Musica/musica acquistata/proseware

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Gestione download**](download-manager.md)
</dt> <dt>

[**DownloadCollection. startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




