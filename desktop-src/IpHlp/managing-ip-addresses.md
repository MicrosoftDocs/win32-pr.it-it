---
description: L'helper IP può facilitare la gestione degli indirizzi IP associati alle interfacce nel computer locale. Usare le funzioni descritte nei paragrafi seguenti per la gestione degli indirizzi IP.
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: Gestione degli indirizzi IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51e0e1e30adf064330a2a4070e6872ca87b50b94e3ad1ab458c3c84878d5549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560321"
---
# <a name="managing-ip-addresses"></a>Gestione degli indirizzi IP

L'helper IP può facilitare la gestione degli indirizzi IP associati alle interfacce nel computer locale. Usare le funzioni descritte nei paragrafi seguenti per la gestione degli indirizzi IP.

La [**funzione GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabella che contiene il mapping degli indirizzi IP alle interfacce. Alla stessa interfaccia possono essere associati più indirizzi IP.

Usare la [**funzione AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere un indirizzo IP a una determinata interfaccia. Per rimuovere gli indirizzi IP aggiunti in precedenza **tramite AddIPAddress,** usare [**la funzione DeleteIPAddress.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)

Le [**funzioni IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) richiedono che il computer locale utilizzi Dynamic Host Configuration Protocol (DHCP). La **funzione IpReleaseAddress** rilascia un indirizzo IP ottenuto in precedenza da DHCP. La **funzione IpRenewAddress** rinnova un lease DHCP in un determinato indirizzo IP. Un lease DHCP consente a un computer di utilizzare un indirizzo IP per un periodo di tempo specificato.

-   Per esempi di codice relativi [**a GetIpAddrTable,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) vedere [Gestione degli indirizzi IP tramite GetIpAddrTable.](managing-ip-addresses-using-getipaddrtable.md)

-   Per esempi di codice [**che coinvolgono AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) [**e DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)vedere Gestione degli indirizzi [IP tramite AddIPAddress e DeleteIPAddress.](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

-   Per esempi di codice [**relativi a IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) vedere Managing [DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).

 

 



