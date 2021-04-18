---
description: La funzione GetTcpStatistics compila un puntatore a una \_ struttura TCPSTATS MIB con informazioni sulle statistiche del protocollo TCP per il computer locale.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Recupero di informazioni tramite GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f4d4d42c2716d258ff72e3dd91ab750baaed20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313364"
---
# <a name="retrieving-information-using-gettcpstatistics"></a><span data-ttu-id="c37b9-103">Recupero di informazioni tramite GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="c37b9-103">Retrieving Information Using GetTcpStatistics</span></span>

<span data-ttu-id="c37b9-104">La funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) compila un puntatore a una struttura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) con informazioni sulle statistiche del protocollo TCP per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="c37b9-104">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function fills a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure with information on the TCP protocol statistics for the local computer.</span></span>

<span data-ttu-id="c37b9-105">**Per usare GetTcpStatistics**</span><span class="sxs-lookup"><span data-stu-id="c37b9-105">**To use GetTcpStatistics**</span></span>

1.  <span data-ttu-id="c37b9-106">Dichiarare alcune variabili necessarie.</span><span class="sxs-lookup"><span data-stu-id="c37b9-106">Declare some variables that are needed.</span></span>

    <span data-ttu-id="c37b9-107">Dichiarare una  variabile DWORD `dwRetVal` che verrà usata da per il controllo degli errori delle chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="c37b9-107">Declare a **DWORD** variable `dwRetVal` that will be using for error checking function calls.</span></span> <span data-ttu-id="c37b9-108">Dichiarare un puntatore a una variabile [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) denominata *pTCPStats* e allocare memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="c37b9-108">Declare a pointer to an [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) variable called *pTCPStats*, and allocate memory for the structure.</span></span> <span data-ttu-id="c37b9-109">Verificare che la memoria sia stata allocata.</span><span class="sxs-lookup"><span data-stu-id="c37b9-109">Check that memory could be allocated.</span></span>

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  <span data-ttu-id="c37b9-110">Chiamare la funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) con il parametro *pTCPStats* per recuperare le statistiche TCP per IPv4 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c37b9-110">Call the [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function with the *pTCPStats* parameter to retrieve TCP statistics for IPv4 on the local computer.</span></span> <span data-ttu-id="c37b9-111">Verificare la presenza di errori e restituire il valore di errore nella variabile **DWORD** `dwRetVal` .</span><span class="sxs-lookup"><span data-stu-id="c37b9-111">Check for errors and return the error value in the **DWORD** variable `dwRetVal`.</span></span> <span data-ttu-id="c37b9-112">Se si verifica un errore, la `dwRetVal` variabile può essere utilizzata per il controllo degli errori e la creazione di report più completi.</span><span class="sxs-lookup"><span data-stu-id="c37b9-112">If an error occurs, the `dwRetVal` variable can be used for more extensive error checking and reporting.</span></span>
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  <span data-ttu-id="c37b9-113">Se la chiamata ha avuto esito positivo, accedere ai dati restituiti nell' [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta il parametro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="c37b9-113">If the call was successful, access the data returned in the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) pointed to by the *pTCPStats* parameter.</span></span>
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  <span data-ttu-id="c37b9-114">Liberare la memoria allocata per la struttura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta il parametro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="c37b9-114">Free the memory allocated for the [**MIB\_TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) structure pointed to by the *pTCPStats* parameter.</span></span> <span data-ttu-id="c37b9-115">Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal parametro *pTCPStats* .</span><span class="sxs-lookup"><span data-stu-id="c37b9-115">This should be done once the application no longer needs the data returned by the *pTCPStats* parameter.</span></span>
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

<span data-ttu-id="c37b9-116">Passaggio successivo: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="c37b9-116">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="c37b9-117">Passaggio precedente: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="c37b9-117">Previous Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

## <a name="complete-source-code"></a><span data-ttu-id="c37b9-118">Completa codice sorgente</span><span class="sxs-lookup"><span data-stu-id="c37b9-118">Complete Source Code</span></span>

-   [<span data-ttu-id="c37b9-119">Codice sorgente completo dell'applicazione helper IP</span><span class="sxs-lookup"><span data-stu-id="c37b9-119">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

 

 
