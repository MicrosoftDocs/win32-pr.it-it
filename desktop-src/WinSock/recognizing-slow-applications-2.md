---
description: Questa guida identifica un'applicazione lenta come applicazione Microsoft Windows con prestazioni non associate.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Riconoscimento di applicazioni lente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316999"
---
# <a name="recognizing-slow-applications"></a>Riconoscimento di applicazioni lente

Questa guida identifica un'applicazione *lenta* come applicazione Microsoft Windows con prestazioni non associate. Un'applicazione lenta presenta uno o più dei seguenti sintomi:

-   L'utilizzo della CPU e della rete è basso.

    Il computer sembra essere in attesa di qualcosa. Spesso, l'applicazione è in attesa sulla rete.

-   La disattivazione dell'algoritmo Nagle tramite l' \_ opzione socket TCP NoDelay aumenta le prestazioni.

    Ciò indica altri problemi e non deve essere considerato una soluzione. La disattivazione dell'algoritmo Nagle aumenta l'overhead del protocollo. Non usare questo metodo come correzione per le applicazioni interrotte, solo per indicare che l'applicazione necessita di altro lavoro per la risoluzione dei problemi di prestazioni.

-   L'applicazione presenta un sovraccarico elevato.

    Per calcolare il sovraccarico delle applicazioni, determinare la quantità di dati che si intende trasferire in ogni direzione. Usare quindi netstat e aggiungere (per Ethernet) 60 byte per ogni pacchetto e 500 byte per ogni connessione. Il sovraccarico migliore che è possibile prevedere per lo streaming tramite Ethernet è circa il 6%. Per una connessione modem, il sovraccarico migliore è approssimativamente del 2%, a causa del fatto che un collegamento PPP usa la compressione di intestazione. Per ulteriori informazioni, vedere [calcolo del sovraccarico con netstat](calculating-overhead-with-netstat-2.md) .

-   La risposta dell'applicazione rallenta quando la connessione ha un RTT di grandi dimensioni.

    Supponendo che l'applicazione non si avvicini alla larghezza di banda del collegamento, un RTT di grandi dimensioni deve avere un effetto minimo o nullo. Un notevole rallentamento con un RTT di grandi dimensioni è un segno chiaro dell'elaborazione serializzata e di molte transazioni di piccole dimensioni.

Ogni applicazione deve essere testata in un ambiente con un RTT di grandi dimensioni. In questo modo viene visualizzata la maggior parte delle applicazioni che soffrono di scelte di sviluppo scarse. Questo test può essere eseguito in diversi ambienti, tra cui una rete LAN wireless, un simulatore di ritardo del collegamento o una rete satellite.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comportamento dell'applicazione](application-behavior-2.md)
</dt> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



