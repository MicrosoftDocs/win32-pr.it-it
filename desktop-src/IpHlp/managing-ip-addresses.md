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
# <a name="managing-ip-addresses"></a><span data-ttu-id="75fe7-104">Gestione degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="75fe7-104">Managing IP Addresses</span></span>

<span data-ttu-id="75fe7-105">L'helper IP può semplificare la gestione degli indirizzi IP associati alle interfacce nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="75fe7-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="75fe7-106">Usare le funzioni descritte nei paragrafi seguenti per la gestione degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="75fe7-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="75fe7-107">La funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) recupera una tabella che contiene il mapping degli indirizzi IP alle interfacce.</span><span class="sxs-lookup"><span data-stu-id="75fe7-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="75fe7-108">Più di un indirizzo IP può essere associato alla stessa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="75fe7-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="75fe7-109">Usare la funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere un indirizzo IP a una particolare interfaccia.</span><span class="sxs-lookup"><span data-stu-id="75fe7-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="75fe7-110">Per rimuovere gli indirizzi IP aggiunti in precedenza tramite **AddIpAddress**, usare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .</span><span class="sxs-lookup"><span data-stu-id="75fe7-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="75fe7-111">Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) richiedono che il computer locale usi Dynamic Host Configuration Protocol (DHCP).</span><span class="sxs-lookup"><span data-stu-id="75fe7-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="75fe7-112">La funzione **IpReleaseAddress** rilascia un indirizzo IP ottenuto in precedenza da DHCP.</span><span class="sxs-lookup"><span data-stu-id="75fe7-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="75fe7-113">La funzione **IpRenewAddress** rinnova un lease DHCP su un indirizzo IP specifico.</span><span class="sxs-lookup"><span data-stu-id="75fe7-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="75fe7-114">Un lease DHCP consente a un computer di utilizzare un indirizzo IP per un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="75fe7-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="75fe7-115">Per esempi di codice che coinvolgono [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) , vedere [gestione degli indirizzi IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="75fe7-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="75fe7-116">Per esempi di codice che coinvolgono [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) e [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), vedere [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span><span class="sxs-lookup"><span data-stu-id="75fe7-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="75fe7-117">Per esempi di codice che coinvolgono [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , vedere [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span><span class="sxs-lookup"><span data-stu-id="75fe7-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



