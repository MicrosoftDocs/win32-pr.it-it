---
description: L'helper IP fornisce funzionalità per la gestione del routing di rete. Utilizzare le seguenti funzioni per gestire la tabella di routing IP e per ottenere altre informazioni di routing.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gestione del routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879081"
---
# <a name="managing-routing"></a>Gestione del routing

L'helper IP fornisce funzionalità per la gestione del routing di rete. Utilizzare le seguenti funzioni per gestire la tabella di routing IP e per ottenere altre informazioni di routing.

Recuperare il contenuto della tabella di routing IP effettuando una chiamata alla funzione [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) . Modificare voci specifiche nella tabella di routing IP usando le funzioni [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)e [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) . Utilizzare la funzione **CreateIpForwardEntry** per aggiungere una nuova voce della tabella di routing. Utilizzare la funzione **DeleteIpForwardEntry** per rimuovere una voce esistente. La funzione **SetIpForwardEntry** modifica una voce esistente.

Le funzionalità di gestione del router dell'helper IP possono essere utilizzate per recuperare informazioni sul modo in cui i datagrammi vengono instradati sulla rete. La funzione [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la route migliore a un indirizzo di destinazione specificato. La funzione [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera l'indice dell'interfaccia utilizzata dalla route migliore a un indirizzo di destinazione specificato. Infine, la funzione [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) Recupera il tempo di round trip (RTT) e il numero di hop a un indirizzo di destinazione specificato.

 

 



