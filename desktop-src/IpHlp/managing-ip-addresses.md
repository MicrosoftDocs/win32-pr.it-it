---
description: L'helper IP può semplificare la gestione degli indirizzi IP associati alle interfacce nel computer locale. Usare le funzioni descritte nei paragrafi seguenti per la gestione degli indirizzi IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Gestione degli indirizzi IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306596"
---
# <a name="managing-ip-addresses"></a>Gestione degli indirizzi IP

L'helper IP può semplificare la gestione degli indirizzi IP associati alle interfacce nel computer locale. Usare le funzioni descritte nei paragrafi seguenti per la gestione degli indirizzi IP.

La funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabella che contiene il mapping degli indirizzi IP alle interfacce. Più di un indirizzo IP può essere associato alla stessa interfaccia.

Usare la funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere un indirizzo IP a una particolare interfaccia. Per rimuovere gli indirizzi IP aggiunti in precedenza tramite **AddIpAddress**, usare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) richiedono che il computer locale usi Dynamic Host Configuration Protocol (DHCP). La funzione **IpReleaseAddress** rilascia un indirizzo IP ottenuto in precedenza da DHCP. La funzione **IpRenewAddress** rinnova un lease DHCP su un indirizzo IP specifico. Un lease DHCP consente a un computer di utilizzare un indirizzo IP per un periodo di tempo specificato.

-   Per esempi di codice che coinvolgono [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , vedere [gestione degli indirizzi IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

-   Per esempi di codice che coinvolgono [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) e [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), vedere [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).

-   Per esempi di codice che coinvolgono [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , vedere [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



