---
description: L'helper IP estende le capacità di gestione delle interfacce di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.
ms.assetid: 598bbe67-30df-4c02-8f30-2ccf15b5c494
title: Gestione delle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d79d46ec1ba7606cbc7e79b4312432984239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227413"
---
# <a name="managing-interfaces"></a><span data-ttu-id="8bcff-105">Gestione delle interfacce</span><span class="sxs-lookup"><span data-stu-id="8bcff-105">Managing Interfaces</span></span>

<span data-ttu-id="8bcff-106">L'helper IP estende le capacità di gestione delle interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="8bcff-106">IP Helper extends your abilities to manage network interfaces.</span></span> <span data-ttu-id="8bcff-107">Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="8bcff-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="8bcff-108">Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.</span><span class="sxs-lookup"><span data-stu-id="8bcff-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="8bcff-109">Usare le funzioni descritte nei paragrafi seguenti per gestire le interfacce nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8bcff-109">Use the functions described in the following paragraphs to manage interfaces on the local computer.</span></span>

<span data-ttu-id="8bcff-110">La funzione [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) restituisce il numero di interfacce nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8bcff-110">The [**GetNumberOfInterfaces**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnumberofinterfaces) function returns the number of interfaces on the local computer.</span></span>

<span data-ttu-id="8bcff-111">La funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) restituisce una tabella che contiene i nomi e gli indici corrispondenti per le interfacce nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8bcff-111">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function returns a table that contains the names and corresponding indexes for the interfaces on the local computer.</span></span> <span data-ttu-id="8bcff-112">Per esempi di codice che coinvolgono **GetInterfaceInfo** , vedere [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="8bcff-112">For code samples involving **GetInterfaceInfo** see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="8bcff-113">La funzione [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) accetta un indice di interfaccia e restituisce un indice di interfaccia compatibile con le versioni precedenti, ovvero uno che usa solo i 24 bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="8bcff-113">The [**GetFriendlyIfIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getfriendlyifindex) function takes an interface index and returns a backward-compatible interface index, that is, one that uses only the lower 24 bits.</span></span> <span data-ttu-id="8bcff-114">Questo tipo di indice viene talvolta definito indice di interfaccia "descrittivo".</span><span class="sxs-lookup"><span data-stu-id="8bcff-114">This type of index is sometimes referred to as a "friendly" interface index.</span></span>

<span data-ttu-id="8bcff-115">La funzione [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) restituisce una struttura [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) che contiene informazioni su una particolare interfaccia nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8bcff-115">The [**GetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getifentry) function returns a [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) structure that contains information about a particular interface on the local computer.</span></span> <span data-ttu-id="8bcff-116">Questa funzione richiede che il chiamante fornisca l'indice dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8bcff-116">This function requires the caller to supply the index of the interface.</span></span>

<span data-ttu-id="8bcff-117">La funzione [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) restituisce una tabella di voci [**MIB \_ IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) , una per ogni interfaccia nel computer.</span><span class="sxs-lookup"><span data-stu-id="8bcff-117">The [**GetIfTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getiftable) function returns a table of [**MIB\_IFROW**](/windows/win32/api/ifmib/ns-ifmib-mib_ifrow) entries, one for each interface on the computer.</span></span>

<span data-ttu-id="8bcff-118">Utilizzare la funzione [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) per modificare la configurazione di una particolare interfaccia.</span><span class="sxs-lookup"><span data-stu-id="8bcff-118">Use the [**SetIfEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setifentry) function to modify the configuration of a particular interface.</span></span>

 

 
