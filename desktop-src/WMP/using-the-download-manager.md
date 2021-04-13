---
title: Uso di Download Manager
description: Uso di Download Manager
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online Stores, Download Manager
- archivi online, gestione download
- digitare 2 archivi online, Download Manager
- Windows Media Player, Download Manager
- Gestione download di Windows Media Player
- Gestione download
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396886"
---
# <a name="using-the-download-manager"></a>Uso di Download Manager

Windows Media Player SDK include una pagina Web di esempio che illustra l'utilizzo di gestione download per scaricare i file nel computer dell'utente. È possibile individuare l'esempio nella cartella denominata Web in cui è stato installato l'SDK. Il nome del file è sample. ASP. Nell'esempio sono disponibili le seguenti funzionalità:

-   Crea l'oggetto **downloadmanager** .
-   Crea un oggetto **DownloadCollection** .
-   Inizia a scaricare cinque file quando l'utente fa clic su **download**. Nell'esempio vengono forniti i percorsi di file predefiniti. È necessario sostituire questi percorsi predefiniti con i percorsi dei file nel proprio server. È possibile modificare i percorsi modificando i valori assegnati alla matrice globale denominata g \_ sFiles.
-   Mostra informazioni sullo stato di un download quando l'utente lo seleziona.
-   Fornisce i controlli per sospendere, riprendere, annullare e rimuovere un elemento di download.
-   Mantiene le informazioni sulle raccolte di download tra le sessioni usando i cookie. Questo è importante perché l'utente può chiudere il lettore in qualsiasi momento. Inoltre, se l'utente passa i riquadri attività nel lettore, termina la sessione di archiviazione online.
-   Usa il download in tempo reale per impostazione predefinita. È possibile modificare il comportamento per il download in background modificando il valore della variabile denominata g \_ sDLType. Il download in background è disponibile per l'utilizzo con il sistema operativo Microsoft Windows XP.
-   Sincronizza il colore di sfondo con il colore del lettore. Questa funzionalità può essere usata per modificare l'aspetto del negozio online quando l'utente sceglie di modificare il colore del lettore.

Le sezioni seguenti forniscono altre informazioni:

-   [Inizializzazione della pagina](initializing-the-page.md)
-   [Avvio dei download](starting-the-downloads.md)
-   [Recupero delle informazioni sullo stato](retrieving-status-information.md)
-   [Gestione delle informazioni sulla sessione](maintaining-session-information.md)
-   [Debug della pagina](debugging-the-page.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi online di tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




