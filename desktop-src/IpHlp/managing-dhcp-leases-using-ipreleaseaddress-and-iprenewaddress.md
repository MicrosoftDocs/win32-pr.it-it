---
title: Gestire lease DHCP con IpReleaseAddress, IpRenewAddress
description: Le funzioni IpReleaseAddress e IpRenewAddress vengono utilizzate per rilasciare e rinnovare il lease del Dynamic Host Configuration Protocol corrente (DHCP).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879082"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="5e7f6-103">Gestire lease DHCP con IpReleaseAddress, IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="5e7f6-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="5e7f6-104">Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) vengono utilizzate per rilasciare e rinnovare il lease del Dynamic Host Configuration Protocol corrente (DHCP).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="5e7f6-105">La funzione **IpReleaseAddress** rilascia un indirizzo IPv4 ottenuto in precedenza tramite DHCP.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="5e7f6-106">La funzione **IpRenewAddress** rinnova un lease in un indirizzo IPv4 ottenuto in precedenza tramite DHCP.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="5e7f6-107">È comune usare queste due funzioni insieme, per prima cosa rilasciare il lease con una chiamata a **IpReleaseAddress** e quindi rinnovare il lease con una chiamata alla funzione **IpRenewAddress** .</span><span class="sxs-lookup"><span data-stu-id="5e7f6-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="5e7f6-108">Quando un client DHCP ha ottenuto in precedenza un lease DHCP e [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) non viene chiamato prima della funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , la richiesta del client DHCP viene inviata al server DHCP che ha emesso il lease DHCP iniziale.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="5e7f6-109">Questo server DHCP potrebbe non essere disponibile o la richiesta DHCP potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="5e7f6-110">Quando un host ha ottenuto in precedenza un lease DHCP e **IpReleaseAddress** viene chiamato prima della funzione **IpRenewAddress** , il client DHCP rilascia innanzitutto l'indirizzo IP ottenuto e invia una richiesta del client DHCP per una risposta da qualsiasi server DHCP disponibile.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="5e7f6-111">Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IPRENEWADDRESS**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) richiedono che DHCP sia abilitato per una corretta esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="5e7f6-112">La funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) accetta un puntatore a una struttura della mappa dell' [**indice della \_ scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) come unico parametro.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="5e7f6-113">Per ottenere questo parametro, chiamare prima [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="5e7f6-114">Per informazioni sulla funzione **GetInterfaceInfo** , vedere [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="5e7f6-115">**Per usare IpReleaseAddress**</span><span class="sxs-lookup"><span data-stu-id="5e7f6-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="5e7f6-116">Ottenere un puntatore a una struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) utilizzando la funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="5e7f6-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="5e7f6-117">Per informazioni sulla funzione GetInterfaceInfo, vedere Gestione delle [interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="5e7f6-118">Creare un  oggetto DWORD `dwRetVal` (usato per il controllo degli errori).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="5e7f6-119">Si presuppone che venga chiamata la variabile restituita da **GetInterfaceInfo** `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="5e7f6-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="5e7f6-120">Se DHCP è abilitato, chiamare la funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , passando la variabile della mappa dell' [**\_ \_ indice \_ della scheda IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` come parametro.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="5e7f6-121">Verificare la presenza di errori generali e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="5e7f6-122">La funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) restituisce un parametro che può essere utilizzato per verificare se DHCP è abilitato prima di chiamare queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="5e7f6-123">Per informazioni su **GetAdaptersInfo**, vedere [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="5e7f6-124">È comune usare queste due funzioni insieme, chiamando la funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e quindi chiamando la funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando la stessa struttura del parametro a entrambe le funzioni.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="5e7f6-125">Nella procedura seguente si presuppone che le funzioni non vengano utilizzate insieme; Tuttavia, se le funzioni vengono utilizzate insieme, ignorare il passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="5e7f6-126">**Per usare IpRenewAddress**</span><span class="sxs-lookup"><span data-stu-id="5e7f6-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="5e7f6-127">Ottenere un puntatore a una struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) utilizzando la funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) .</span><span class="sxs-lookup"><span data-stu-id="5e7f6-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="5e7f6-128">Per informazioni sulla funzione **GetInterfaceInfo** , vedere Gestione delle [interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="5e7f6-129">Dichiarare un  oggetto DWORD `dwRetVal` (usato per il controllo degli errori) se questa variabile non è stata dichiarata.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="5e7f6-130">Si presuppone che venga chiamata la variabile restituita da **GetInterfaceInfo** `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="5e7f6-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="5e7f6-131">Chiamare la funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando la variabile della mappa dell' [**\_ \_ indice \_ dell'adattatore IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` come parametro.</span><span class="sxs-lookup"><span data-stu-id="5e7f6-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="5e7f6-132">Verificare la presenza di errori generali e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).</span><span class="sxs-lookup"><span data-stu-id="5e7f6-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="5e7f6-133">Passaggio successivo: [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="5e7f6-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="5e7f6-134">Passaggio precedente: [gestione degli indirizzi IP con GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="5e7f6-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



