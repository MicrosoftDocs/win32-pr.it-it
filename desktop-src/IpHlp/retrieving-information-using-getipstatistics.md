---
description: La funzione GetIpStatistics riempie un puntatore a una struttura IPSTATS MIB con informazioni sulle statistiche IP correnti \_ associate al sistema.
ms.assetid: 2b65a817-3f80-426f-ada0-bf4b34a410ed
title: Recupero di informazioni tramite GetIpStatistics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c383c49b316eb48e240a8272957dae8ee3ec1671304df8d466b869b7bf4ec0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050271"
---
# <a name="retrieving-information-using-getipstatistics"></a>Recupero di informazioni tramite GetIpStatistics

La [**funzione GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) riempie un puntatore a una struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) con informazioni sulle statistiche IP correnti associate al sistema.

**Per usare GetIpStatistics**

1.  Dichiarare alcune variabili necessarie.

    Dichiarare una **variabile DWORD** che `dwRetval` verrà utilizzata per le chiamate di funzione di controllo degli errori. Dichiarare un puntatore a [**una variabile \_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominata *pStats* e allocare memoria per la struttura. Verificare che sia possibile allocare memoria.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Chiamare la [**funzione GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con il *parametro pStats* per recuperare le statistiche IP per il computer locale. Verificare la presenza di errori e restituire il valore di errore nella **variabile DWORD** `dwRetval` . Se si verifica un errore, la variabile può essere utilizzata per il controllo degli errori e la creazione di report `dwRetval` più estesi.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Se la chiamata a [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) ha avuto esito positivo, stampare alcuni dei dati nella struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta *il parametro pStats.*
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Liberare la memoria allocata per [**la struttura \_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta *il parametro pStats.* Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal *parametro pStats.*
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Passaggio successivo: [Recupero di informazioni tramite GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Passaggio precedente: [Gestione degli indirizzi IP con AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
