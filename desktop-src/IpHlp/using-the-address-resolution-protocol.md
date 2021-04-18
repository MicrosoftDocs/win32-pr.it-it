---
description: È possibile utilizzare Helper IP per eseguire operazioni ARP (Address Resolution Protocol) per il computer locale. Usare le funzioni seguenti per recuperare e modificare la tabella ARP.
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: Uso del protocollo di risoluzione degli indirizzi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318299"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="dc9e9-104">Uso del protocollo di risoluzione degli indirizzi</span><span class="sxs-lookup"><span data-stu-id="dc9e9-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="dc9e9-105">È possibile utilizzare Helper IP per eseguire operazioni ARP (Address Resolution Protocol) per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="dc9e9-106">Usare le funzioni seguenti per recuperare e modificare la tabella ARP.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="dc9e9-107">[**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) recupera la tabella ARP.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="dc9e9-108">La tabella ARP contiene il mapping degli indirizzi IP agli indirizzi fisici.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="dc9e9-109">Gli indirizzi fisici vengono talvolta definiti indirizzi MAC (Media Access Controller).</span><span class="sxs-lookup"><span data-stu-id="dc9e9-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="dc9e9-110">Utilizzare le funzioni [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) e [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) per aggiungere o rimuovere voci ARP specifiche da o verso la tabella.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="dc9e9-111">La funzione [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) Elimina tutte le voci dalla tabella.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="dc9e9-112">Per creare o eliminare le voci ARP proxy, usare le funzioni [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) e [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) .</span><span class="sxs-lookup"><span data-stu-id="dc9e9-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="dc9e9-113">La funzione [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) invia una richiesta ARP alla rete locale.</span><span class="sxs-lookup"><span data-stu-id="dc9e9-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



