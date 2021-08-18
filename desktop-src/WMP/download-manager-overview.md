---
title: Panoramica di Download Manager
description: Panoramica di Download Manager
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player online store, Download Manager
- negozi online, Download Manager
- Store online di tipo 2, Download Manager
- Windows Media Player negozi online, download in tempo reale
- negozi online, download in tempo reale
- tipo 2 negozi online, download in tempo reale
- Windows Media Player negozi online, download in background
- negozi online, download in background
- tipo 2 negozi online, download in background
- Windows Media Player,Download Manager
- Windows Media Player Download Manager
- Download Manager
- download in tempo reale
- download in background
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790466db4c09f7c2310729bd6f866bc5066348641a73756eb9199aa685a7fafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997081"
---
# <a name="download-manager-overview"></a>Panoramica di Download Manager

Microsoft Windows Media Player i riquadri attività del negozio online che contengono una finestra del browser ospitata. Tramite i negozi online, gli utenti possono interagire con le pagine Web dei negozi online su Internet.

Gestione Windows Media Player download fornisce un modello a oggetti che è possibile usare per gestire le attività associate al download di contenuto nel computer dell'utente da Microsoft Internet Information Services (IIS) usando Hypertext Transfer Protocol (HTTP). Con Download Manager è possibile:

-   Gestire più download contemporaneamente come raccolta.
-   Specificare un URL per un file e avviarne il download tramite HTTP.
-   Eseguire una query per lo stato e lo stato di download.
-   Sospendere, riprendere o annullare un download.
-   Specificare se un download viene eseguito in background o in tempo reale. Il download in background è disponibile solo nel sistema operativo Microsoft Windows XP. Vedere [Informazioni sul download in background e in tempo reale.](#about-background-and-real-time-downloading)
-   Specificare la modalità di visualizzazione del contenuto nella libreria. Vedere [Informazioni sull'integrazione della libreria.](#about-library-integration)

Download Manager è la soluzione per il download di contenuto dal codice script nelle pagine Web ospitate. Per scaricare contenuto usando il codice C++, usare Windows XP Servizio trasferimento intelligente in background (BITS). Per altre informazioni, vedere [BITS](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Informazioni sul download in background e in tempo reale

Download Manager offre due tipi di download: in background e in tempo reale. Il tipo che si usa è quello che si sceglie ed è possibile consentire all'utente di selezionare anche il tipo di download. Se si sceglie di consentire all'utente di selezionare il tipo di download, assicurarsi di spiegare le differenze tra i due tipi disponibili.

Il download in tempo reale avviene tutto in una volta. Quando l'utente avvia un download di file, l'intero file viene trasferito al computer dell'utente in un unico flusso continuo. L'utente non può sospendere o interrompere in altro modo il download. Se l'utente sceglie di chiudere Windows Media Player il download, perde tutti i file incompleti e deve scaricarli dall'inizio per acquisire il contenuto.

Il vantaggio principale del download in tempo reale è che consente all'utente di acquisire il contenuto più velocemente rispetto al download in background. Il download in tempo reale è disponibile per gli utenti di Windows XP, ma è l'unico tipo di download disponibile nelle versioni del sistema operativo Windows prima di Windows XP.

Il download in background avviene in modo frammentato. Quando l'utente avvia un download in background, parti del file vengono trasferite al computer dell'utente quando è disponibile il tempo del processore. È possibile sospendere e riprendere un download in background. Se l'utente sceglie di chiudere il Windows Media Player prima del completamento del download in background, la condizione di tutti i file incompleti viene salvata e il download può continuare in background, anche dopo il riavvio del computer.

Il download in background può richiedere più tempo del download in tempo reale perché il processo di download si verifica solo quando il processore non esegue altre attività.

Il download in background è disponibile solo quando si usa Windows XP.

## <a name="about-library-integration"></a>Informazioni sull'integrazione della libreria

Windows Media Player possibile organizzare automaticamente il contenuto del negozio online nella libreria. Per abilitare questa funzionalità, è necessario specificare un valore per **l'attributo WM/ContentDistributor** per ogni file multimediale digitale. Quando un file multimediale digitale viene aggiunto alla libreria, che si verifica automaticamente quando si usa Download Manager, il file viene elencato automaticamente nel nodo **Purchased Musica** or **Purchased Videos** (Video acquistati). Ad esempio, se il valore di **WM/ContentDistributor** è "Proseware" e il file multimediale digitale contiene musica, il contenuto verrà visualizzato nella libreria nel percorso seguente:

Tutti Musica/Acquistati Musica/Proseware

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Download Manager**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




