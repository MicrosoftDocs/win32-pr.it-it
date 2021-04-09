---
description: L'helper IP fornisce funzionalità di recupero delle informazioni utili per l'amministrazione di rete del computer locale.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966433"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a>Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol

L'helper IP fornisce funzionalità di recupero delle informazioni utili per l'amministrazione di rete del computer locale. Le funzioni seguenti recuperano le statistiche per il protocollo IP (Internet Protocol) e il Internet Control Message Protocol (ICMP). È anche possibile usare queste funzioni per impostare determinati parametri di configurazione per l'indirizzo IP.

La funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera le statistiche IP correnti per il computer locale. Per esempi di codice che coinvolgono **GetIPStatistics** , vedere [recupero di informazioni con GetIPStatistics](retrieving-information-using-getipstatistics.md).

La funzione [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera le statistiche ICMP correnti.

Usare la funzione [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) per abilitare o disabilitare l'invio di indirizzi IP. Questa funzione consente inoltre di impostare la durata (TTL) predefinita per i datagrammi IP. In alternativa, è possibile impostare la durata (TTL) utilizzando la funzione [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .

 

 



