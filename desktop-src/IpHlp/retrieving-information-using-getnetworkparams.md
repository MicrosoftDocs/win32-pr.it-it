---
description: Inserisce un puntatore a una struttura di \_ informazioni fisse con i dati sulle impostazioni di rete correnti.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Recupero di informazioni tramite GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20aed9b1ffa761ec53637d4d5b165e3fd2c2673d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231888"
---
# <a name="retrieving-information-using-getnetworkparams"></a><span data-ttu-id="38c47-103">Recupero di informazioni tramite GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="38c47-103">Retrieving Information Using GetNetworkParams</span></span>

<span data-ttu-id="38c47-104">La funzione [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) compila un puntatore a una struttura [**di \_ informazioni fisse**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) con i dati sulle impostazioni di rete correnti.</span><span class="sxs-lookup"><span data-stu-id="38c47-104">The [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function fills a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) structure with data about the current network settings.</span></span>

<span data-ttu-id="38c47-105">**Per usare GetNetworkParams**</span><span class="sxs-lookup"><span data-stu-id="38c47-105">**To use GetNetworkParams**</span></span>

1.  <span data-ttu-id="38c47-106">Dichiarare un puntatore a un [**oggetto \_ info fisso**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) denominato *PFixedInfo* e un oggetto **ULONG** denominato *ulOutBufLen*.</span><span class="sxs-lookup"><span data-stu-id="38c47-106">Declare a pointer to a [**FIXED\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) object called *pFixedInfo*, and a **ULONG** object called *ulOutBufLen*.</span></span> <span data-ttu-id="38c47-107">Queste variabili vengono passate come parametri alla funzione [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) .</span><span class="sxs-lookup"><span data-stu-id="38c47-107">These variables are passed as parameters to the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="38c47-108">Creare anche una  variabile DWORD *dwRetVal* (usata per il controllo degli errori).</span><span class="sxs-lookup"><span data-stu-id="38c47-108">Also create a **DWORD** variable *dwRetVal* (used for error checking).</span></span>
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  <span data-ttu-id="38c47-109">Allocare memoria per le strutture.</span><span class="sxs-lookup"><span data-stu-id="38c47-109">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="38c47-110">Le dimensioni di *ulOutBufLen* non sono sufficienti per conservare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="38c47-110">The size of *ulOutBufLen* is not sufficient to hold the information.</span></span> <span data-ttu-id="38c47-111">Vedere il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="38c47-111">See the next step.</span></span>

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  <span data-ttu-id="38c47-112">Eseguire una chiamata iniziale a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) per ottenere le dimensioni necessarie per la variabile *ulOutBufLen* .</span><span class="sxs-lookup"><span data-stu-id="38c47-112">Make an initial call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) to get the size required for the *ulOutBufLen* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="38c47-113">Questa funzione di funzione avrà esito negativo e verrà usata per garantire che la variabile *ulOutBufLen* specifichi una dimensione sufficiente per contenere tutti i dati restituiti a *pFixedInfo*.</span><span class="sxs-lookup"><span data-stu-id="38c47-113">This function function will fail, and is used to ensure that the *ulOutBufLen* variable specifies a size sufficient for holding all the data returned to *pFixedInfo*.</span></span> <span data-ttu-id="38c47-114">Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="38c47-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  <span data-ttu-id="38c47-115">Eseguire una seconda chiamata a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) usando il controllo generale degli errori e restituendo il valore alla variabile **DWORD** *dwRetVal*; utilizzato per la verifica degli errori più avanzata.</span><span class="sxs-lookup"><span data-stu-id="38c47-115">Make a second call to [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) using general error checking and returning its value to the **DWORD** variable *dwRetVal*; used for more advanced error checking.</span></span>
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  <span data-ttu-id="38c47-116">Se la chiamata ha avuto esito positivo, accedere ai dati dalla struttura di dati *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="38c47-116">If the call was successful, access the data from the *pFixedInfo* data structure.</span></span>
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  <span data-ttu-id="38c47-117">Liberare la memoria allocata per la struttura *pFixedInfo* .</span><span class="sxs-lookup"><span data-stu-id="38c47-117">Free any memory allocated for the *pFixedInfo* structure.</span></span>
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

<span data-ttu-id="38c47-118">Passaggio successivo: [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="38c47-118">Next Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

<span data-ttu-id="38c47-119">Passaggio precedente: [creazione di un'applicazione helper IP di base](creating-a-basic-ip-helper-application.md)</span><span class="sxs-lookup"><span data-stu-id="38c47-119">Previous Step: [Creating a Basic IP Helper Application](creating-a-basic-ip-helper-application.md)</span></span>

 

 



