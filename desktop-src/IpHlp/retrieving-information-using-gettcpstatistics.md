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
# <a name="retrieving-information-using-gettcpstatistics"></a>Recupero di informazioni tramite GetTcpStatistics

La funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) compila un puntatore a una struttura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) con informazioni sulle statistiche del protocollo TCP per il computer locale.

**Per usare GetTcpStatistics**

1.  Dichiarare alcune variabili necessarie.

    Dichiarare una  variabile DWORD `dwRetVal` che verrà usata da per il controllo degli errori delle chiamate di funzione. Dichiarare un puntatore a una variabile [**MIB \_ TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) denominata *pTCPStats* e allocare memoria per la struttura. Verificare che la memoria sia stata allocata.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Chiamare la funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) con il parametro *pTCPStats* per recuperare le statistiche TCP per IPv4 nel computer locale. Verificare la presenza di errori e restituire il valore di errore nella variabile **DWORD** `dwRetVal` . Se si verifica un errore, la `dwRetVal` variabile può essere utilizzata per il controllo degli errori e la creazione di report più completi.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Se la chiamata ha avuto esito positivo, accedere ai dati restituiti nell' [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta il parametro *pTCPStats* .
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Liberare la memoria allocata per la struttura [**\_ TCPSTATS MIB**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta il parametro *pTCPStats* . Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal parametro *pTCPStats* .
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Passaggio successivo: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)

Passaggio precedente: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Completa codice sorgente

-   [Codice sorgente completo dell'applicazione helper IP](complete-ip-helper-application-source-code.md)

 

 
