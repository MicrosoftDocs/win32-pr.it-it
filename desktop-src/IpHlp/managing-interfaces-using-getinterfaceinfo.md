---
description: La funzione GetInterfaceInfo compila un puntatore a una struttura di \_ \_ informazioni sull'interfaccia IP con informazioni sulle interfacce associate al sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gestione delle interfacce mediante GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306595"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="0690d-103">Gestione delle interfacce mediante GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="0690d-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="0690d-104">La funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) compila un puntatore a una struttura [**di \_ \_ informazioni sull'interfaccia IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con informazioni sulle interfacce associate al sistema.</span><span class="sxs-lookup"><span data-stu-id="0690d-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="0690d-105">**Per usare GetInterfaceInfo**</span><span class="sxs-lookup"><span data-stu-id="0690d-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="0690d-106">Dichiarare un puntatore a un [**oggetto \_ \_ info dell'interfaccia IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominato `pInfo` e un oggetto **ULONG** denominato `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="0690d-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="0690d-107">Dichiarare anche un oggetto **DWORD** denominato `dwRetVal` (usato per il controllo degli errori).</span><span class="sxs-lookup"><span data-stu-id="0690d-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="0690d-108">Allocare memoria per le strutture.</span><span class="sxs-lookup"><span data-stu-id="0690d-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="0690d-109">La dimensione di `ulOutBufLen` non è sufficiente per conservare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0690d-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="0690d-110">Vedere il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="0690d-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="0690d-111">Eseguire una chiamata iniziale a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) per ottenere le dimensioni necessarie nella `ulOutBufLen` variabile.</span><span class="sxs-lookup"><span data-stu-id="0690d-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="0690d-112">Questa chiamata alla funzione deve avere esito negativo e viene usata per garantire che la `ulOutBufLen` variabile specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="0690d-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="0690d-113">Si tratta di un modello di programmazione comune nell'helper IP per le strutture di dati e le funzioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="0690d-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="0690d-114">Eseguire una seconda chiamata a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con il controllo generale degli errori e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più avanzato).</span><span class="sxs-lookup"><span data-stu-id="0690d-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="0690d-115">Se la chiamata ha avuto esito positivo, accedere ai dati dalla `pInfo` struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="0690d-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="0690d-116">% WS nella prima riga indica una stringa di caratteri "wide".</span><span class="sxs-lookup"><span data-stu-id="0690d-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="0690d-117">Questa operazione viene utilizzata perché l'attributo **Name** della struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` è un **WCHAR**, ovvero una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="0690d-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="0690d-118">Liberare la memoria allocata per la struttura *pInfo* .</span><span class="sxs-lookup"><span data-stu-id="0690d-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="0690d-119">Passaggio successivo: [gestione degli indirizzi IP con GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="0690d-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="0690d-120">Passaggio precedente: [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="0690d-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



