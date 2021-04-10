---
description: La funzione GetAdaptersInfo compila un puntatore a una struttura di \_ \_ informazioni della scheda IP con informazioni sulle schede di rete associate al sistema.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gestione delle schede di rete con GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470e0ce7682a86b29df912fa4d4b1297c2263382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057886"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a><span data-ttu-id="d1aae-103">Gestione delle schede di rete con GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="d1aae-103">Managing Network Adapters Using GetAdaptersInfo</span></span>

<span data-ttu-id="d1aae-104">La funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) compila un puntatore a una struttura [**di \_ \_ informazioni della scheda IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) con informazioni sulle schede di rete associate al sistema.</span><span class="sxs-lookup"><span data-stu-id="d1aae-104">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function fills a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structure with information about the network adapters associated with the system.</span></span>

<span data-ttu-id="d1aae-105">**Per usare GetAdaptersInfo**</span><span class="sxs-lookup"><span data-stu-id="d1aae-105">**To use GetAdaptersInfo**</span></span>

1.  <span data-ttu-id="d1aae-106">Dichiarare un puntatore a una variabile di [**\_ \_ informazioni della scheda IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) denominata *pAdapterInfo* e una variabile **ULONG** denominata *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="d1aae-106">Declare a pointer to an [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) variable called *pAdapterInfo*, and a **ULONG** variable called *ulOutBufLen*.</span></span> <span data-ttu-id="d1aae-107">Queste variabili vengono passate come parametri alla funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="d1aae-107">These variables are passed as parameters to the [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function.</span></span> <span data-ttu-id="d1aae-108">Creare anche una variabile **DWORD** denominata *dwRetVal* (per il controllo degli errori).</span><span class="sxs-lookup"><span data-stu-id="d1aae-108">Also create a **DWORD** variable called *dwRetVal* (for error checking).</span></span>
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="d1aae-109">Allocare memoria per le strutture.</span><span class="sxs-lookup"><span data-stu-id="d1aae-109">Allocate memory for the structures.</span></span>
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  <span data-ttu-id="d1aae-110">Eseguire una chiamata iniziale a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) per ottenere le dimensioni necessarie nella variabile *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="d1aae-110">Make an initial call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) to get the size needed into the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="d1aae-111">Questa chiamata alla funzione deve avere esito negativo e viene usata per garantire che la variabile *ulOutBufLen* specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a *pAdapterInfo*.</span><span class="sxs-lookup"><span data-stu-id="d1aae-111">This call to the function is meant to fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the information returned to *pAdapterInfo*.</span></span> <span data-ttu-id="d1aae-112">Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="d1aae-112">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  <span data-ttu-id="d1aae-113">Eseguire una seconda chiamata a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passando *pAdapterInfo* e *ulOutBufLen* come parametri ed eseguendo il controllo generale degli errori.</span><span class="sxs-lookup"><span data-stu-id="d1aae-113">Make a second call to [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passing *pAdapterInfo* and *ulOutBufLen* as parameters and doing general error checking.</span></span> <span data-ttu-id="d1aae-114">Restituisce il relativo valore alla  variabile DWORD *dwRetVal* (per il controllo degli errori più completo).</span><span class="sxs-lookup"><span data-stu-id="d1aae-114">Return its value to the **DWORD** variable *dwRetVal* (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  <span data-ttu-id="d1aae-115">Se la chiamata ha avuto esito positivo, accedere ad alcuni dati nella struttura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="d1aae-115">If the call was successful, access some of the data in the *pAdapterInfo* structure.</span></span>
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  <span data-ttu-id="d1aae-116">Liberare la memoria allocata per la struttura *pAdapterInfo* .</span><span class="sxs-lookup"><span data-stu-id="d1aae-116">Free any memory allocated for the *pAdapterInfo* structure.</span></span>
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

<span data-ttu-id="d1aae-117">Passaggio successivo: [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="d1aae-117">Next Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

<span data-ttu-id="d1aae-118">Passaggio precedente: [recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="d1aae-118">Previous Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 



