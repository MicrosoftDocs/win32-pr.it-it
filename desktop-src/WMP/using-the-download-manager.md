---
title: Uso di Download Manager
description: Uso di Download Manager
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player store online, Download Manager
- online store, Download Manager
- store online di tipo 2, Download Manager
- Windows Media Player, Download Manager
- Windows Media Player Download Manager
- Download Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a271849e22d17ec406cea24aa0afb92631bf533b39ea2beb45d5cc74b635d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830709"
---
# <a name="using-the-download-manager"></a>Uso di Download Manager

L Windows Media Player SDK include una pagina Web di esempio che illustra l'uso di Download Manager per scaricare i file nel computer dell'utente. È possibile individuare l'esempio nella cartella denominata WebPage in cui è stato installato l'SDK. Il nome del file è sample.asp. L'esempio fornisce le funzionalità seguenti:

-   Crea **l'oggetto DownloadManager.**
-   Crea un **oggetto DownloadCollection.**
-   Avvia il download di cinque file quando l'utente fa clic **su Scarica**. Nell'esempio vengono forniti percorsi di file predefiniti. È consigliabile sostituire questi percorsi predefiniti con i percorsi dei file nel proprio server. È possibile modificare i percorsi modificando i valori assegnati alla matrice globale denominata g \_ sFiles.
-   Visualizza le informazioni sullo stato di un download quando l'utente lo seleziona.
-   Fornisce controlli per sospendere, riprendere, annullare e rimuovere un elemento di download.
-   Gestisce le informazioni sulle raccolte di download tra sessioni tramite cookie. Questo è importante perché l'utente può chiudere il lettore in qualsiasi momento. Inoltre, se l'utente passa da un riquadro attività all'altro nel lettore, la sessione dello store online termina.
-   Usa il download in tempo reale per impostazione predefinita. È possibile modificare il comportamento del download in background modificando il valore della variabile denominata g \_ sDLType. Il download in background è disponibile per l'uso con il sistema operativo Microsoft Windows XP.
-   Sincronizza il colore di sfondo con il colore del lettore. È possibile usare questa funzionalità per modificare l'aspetto del negozio online quando l'utente sceglie di modificare il colore del lettore.

Le sezioni seguenti forniscono altre informazioni:

-   [Inizializzazione della pagina](initializing-the-page.md)
-   [Avvio dei download](starting-the-downloads.md)
-   [Recupero di informazioni sullo stato](retrieving-status-information.md)
-   [Gestione delle informazioni sulla sessione](maintaining-session-information.md)
-   [Debug della pagina](debugging-the-page.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di programmazione per gli store online di tipo 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




