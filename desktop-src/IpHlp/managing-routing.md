---
description: L'helper IP offre funzionalità per gestire il routing di rete. Usare le funzioni seguenti per gestire la tabella di routing IP e per ottenere altre informazioni di routing.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gestione del routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3b351882e08be3d09615acd033e0fb86192aee8675e8f52c4812a1eba398ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146644"
---
# <a name="managing-routing"></a>Gestione del routing

L'helper IP offre funzionalità per gestire il routing di rete. Usare le funzioni seguenti per gestire la tabella di routing IP e per ottenere altre informazioni di routing.

Recuperare il contenuto della tabella di routing IP effettuando una chiamata alla [**funzione GetIpForwardTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) Modificare voci specifiche nella tabella di routing IP usando [**le funzioni CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)e [**SetIpForwardEntry.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) Usare la **funzione CreateIpForwardEntry** per aggiungere una nuova voce della tabella di routing. Usare la **funzione DeleteIpForwardEntry** per rimuovere una voce esistente. La **funzione SetIpForwardEntry** modifica una voce esistente.

Le funzionalità di gestione router dell'helper IP possono essere usate per recuperare informazioni sul modo in cui i datagrammi vengono instradati in rete. La [**funzione GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la route migliore per un indirizzo di destinazione specificato. La [**funzione GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera l'indice dell'interfaccia usata dalla route migliore a un indirizzo di destinazione specificato. Infine, la [**funzione GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) recupera il tempo di round trip (RTT) e il numero di hop a un indirizzo di destinazione specificato.

 

 



