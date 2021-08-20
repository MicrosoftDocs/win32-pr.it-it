---
description: La funzione GetTcpStatistics riempie un puntatore a una struttura MIB TCPSTATS con informazioni sulle statistiche del protocollo \_ TCP per il computer locale.
ms.assetid: cb405d46-cf3e-4f3c-870a-935a0cc8118f
title: Recupero di informazioni tramite GetTcpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb51b1a71c9dc0ff98a40c31894aa3fcf8c0c0ace7b6b05812940cb9808cced
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146594"
---
# <a name="retrieving-information-using-gettcpstatistics"></a>Recupero di informazioni tramite GetTcpStatistics

La [**funzione GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) riempie un puntatore a una struttura [**\_ MIB TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) con informazioni sulle statistiche del protocollo TCP per il computer locale.

**Per usare GetTcpStatistics**

1.  Dichiarare alcune variabili necessarie.

    Dichiarare una **variabile DWORD** che `dwRetVal` verrà utilizzata per le chiamate di funzione di controllo degli errori. Dichiarare un puntatore a [**una variabile \_ MIB TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) denominata *pTCPStats* e allocare memoria per la struttura. Verificare che sia possibile allocare memoria.

    ```C++
    DWORD dwRetVal = 0;
    PMIB_TCPSTATS pTCPStats;

    pTCPStats = (MIB_TCPSTATS *) malloc(sizeof (MIB_TCPSTATS));
    if (pTCPStats == NULL) {
        printf("Error allocating memory\n");
    }
    ```

    

2.  Chiamare la [**funzione GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) con il *parametro pTCPStats* per recuperare le statistiche TCP per IPv4 nel computer locale. Verificare la presenza di errori e restituire il valore di errore nella **variabile DWORD** `dwRetVal` . Se si verifica un errore, la variabile può essere utilizzata per il controllo degli errori e la creazione di report `dwRetVal` più estesi.
    ```C++
        if ((dwRetVal = GetTcpStatistics(pTCPStats)) != NO_ERROR) {
            printf("GetTcpStatistics failed with error: %ld\n", dwRetVal);
        } 
    ```

    

3.  Se la chiamata ha esito positivo, accedere ai dati restituiti in [**\_ MIB TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta *il parametro pTCPStats.*
    ```C++
    printf("\tNumber of active opens:  %u\n", pTCPStats->dwActiveOpens);
    printf("\tNumber of passive opens: %u\n", pTCPStats->dwPassiveOpens);
    printf("\tNumber of segments received: %u\n", pTCPStats->dwInSegs);
    printf("\tNumber of segments transmitted: %u\n", pTCPStats->dwOutSegs);
    printf("\tNumber of total connections: %u\n", pTCPStats->dwNumConns);
    ```

    

4.  Liberare la memoria allocata [**per la struttura \_ MIB TCPSTATS**](/windows/win32/api/tcpmib/ns-tcpmib-mib_tcpstats_lh) a cui punta *il parametro pTCPStats.* Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal *parametro pTCPStats.*
    ```C++
    if (pTCPStats)
        free(pTCPStats);
    ```

    

Passaggio successivo: [Recupero di informazioni tramite GetIpStatistics](retrieving-information-using-getipstatistics.md)

Passaggio precedente: [Recupero di informazioni tramite GetIpStatistics](retrieving-information-using-getipstatistics.md)

## <a name="complete-source-code"></a>Codice sorgente completo

-   [Codice sorgente completo dell'applicazione helper IP](complete-ip-helper-application-source-code.md)

 

 
