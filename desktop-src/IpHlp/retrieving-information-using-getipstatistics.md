---
description: La funzione GetIpStatistics compila un puntatore a una \_ struttura IPSTATS MIB con informazioni sulle statistiche IP correnti associate al sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recupero di informazioni tramite GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6267c3939548c8f8ea9ab2705ea1769360748e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313366"
---
# <a name="retrieving-information-using-getipstatistics"></a><span data-ttu-id="15986-103">Recupero di informazioni tramite GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="15986-103">Retrieving Information Using GetIpStatistics</span></span>

<span data-ttu-id="15986-104">La funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) compila un puntatore a una struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) con informazioni sulle statistiche IP correnti associate al sistema.</span><span class="sxs-lookup"><span data-stu-id="15986-104">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function fills a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure with information about the current IP statistics associated with the system.</span></span>

<span data-ttu-id="15986-105">**Per usare GetIpStatistics**</span><span class="sxs-lookup"><span data-stu-id="15986-105">**To use GetIpStatistics**</span></span>

1.  <span data-ttu-id="15986-106">Dichiarare alcune variabili necessarie.</span><span class="sxs-lookup"><span data-stu-id="15986-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="15986-107">Dichiarare una  variabile DWORD `dwRetval` che verrà usata da per il controllo degli errori delle chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="15986-107">Declare a **DWORD** variable `dwRetval` that will be using for error checking function calls.</span></span> <span data-ttu-id="15986-108">Dichiarare un puntatore a una variabile [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominata *pStats* e allocare memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="15986-108">Declare a pointer to an [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) variable called *pStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="15986-109">Verificare che la memoria sia stata allocata.</span><span class="sxs-lookup"><span data-stu-id="15986-109">Check that memory could be allocated.</span></span>

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  <span data-ttu-id="15986-110">Chiamare la funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con il parametro *pStats* per recuperare le statistiche IP per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="15986-110">Call the [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function with the *pStats* parameter to retrieve IP statistics for the local computer.</span></span> <span data-ttu-id="15986-111">Verificare la presenza di errori e restituire il valore di errore nella variabile **DWORD** `dwRetval` .</span><span class="sxs-lookup"><span data-stu-id="15986-111">Check for errors and return the error value in the **DWORD** variable `dwRetval`.</span></span> <span data-ttu-id="15986-112">Se si verifica un errore, la `dwRetval` variabile può essere utilizzata per il controllo degli errori e la creazione di report più completi.</span><span class="sxs-lookup"><span data-stu-id="15986-112">If an error occurs, the `dwRetval` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  <span data-ttu-id="15986-113">Se la chiamata a [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) ha avuto esito positivo, stampare alcuni dati nella struttura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta il parametro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="15986-113">If the call to [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) was successful, print out some of the data in the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span>
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  <span data-ttu-id="15986-114">Liberare la memoria allocata per la struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta il parametro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="15986-114">Free the memory allocated for the [**MIB\_IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) structure pointed to by the *pStats* parameter.</span></span> <span data-ttu-id="15986-115">Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal parametro *pStats* .</span><span class="sxs-lookup"><span data-stu-id="15986-115">This should be done once the application no longer needs the data returned by the *pStats* parameter.</span></span>
    ```C++
    if (pStats)
        free(pStats);
    ```

    

<span data-ttu-id="15986-116">Passaggio successivo: [recupero di informazioni tramite GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="15986-116">Next Step: [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)</span></span>

<span data-ttu-id="15986-117">Passaggio precedente: [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="15986-117">Previous Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

 

 
