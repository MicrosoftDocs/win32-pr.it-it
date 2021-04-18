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
# <a name="retrieving-information-using-getipstatistics"></a>Recupero di informazioni tramite GetIpStatistics

La funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) compila un puntatore a una struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) con informazioni sulle statistiche IP correnti associate al sistema.

**Per usare GetIpStatistics**

1.  Dichiarare alcune variabili necessarie.

    Dichiarare una  variabile DWORD `dwRetval` che verrà usata da per il controllo degli errori delle chiamate di funzione. Dichiarare un puntatore a una variabile [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) denominata *pStats* e allocare memoria per la struttura. Verificare che la memoria sia stata allocata.

    ```C++
    MIB_IPSTATS  *pStats;
    DWORD        dwRetVal = 0;

    pStats = (MIB_IPSTATS*) malloc(sizeof(MIB_IPSTATS));

    if (pStats == NULL) {
        printf("Unable to allocate memory for MIB_IPSTATS\n");
    }
    ```

    

2.  Chiamare la funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) con il parametro *pStats* per recuperare le statistiche IP per il computer locale. Verificare la presenza di errori e restituire il valore di errore nella variabile **DWORD** `dwRetval` . Se si verifica un errore, la `dwRetval` variabile può essere utilizzata per il controllo degli errori e la creazione di report più completi.
    ```C++
    dwRetVal = GetIpStatistics(pStats);
    if (dwRetVal != NO_ERROR) {
        printf("GetIpStatistics call failed with %d\n", dwRetVal);
    }
    ```

    

3.  Se la chiamata a [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) ha avuto esito positivo, stampare alcuni dati nella struttura [**MIB \_ IPSTATS**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta il parametro *pStats* .
    ```C++
    printf("Number of interfaces:   %ld\n", pStats->dwNumIf);
    printf("Number of IP addresses: %ld\n", pStats->dwNumAddr);
    printf("Number of received datagrams:  %ld\n", pStats->dwInReceives);
    printf("NUmber of outgoing datagrams requested to transmit:  %ld\n", pStats->dwOutRequests);
    ```

    

4.  Liberare la memoria allocata per la struttura [**\_ IPSTATS MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipstats_lh) a cui punta il parametro *pStats* . Questa operazione deve essere eseguita quando l'applicazione non necessita più dei dati restituiti dal parametro *pStats* .
    ```C++
    if (pStats)
        free(pStats);
    ```

    

Passaggio successivo: [recupero di informazioni tramite GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Passaggio precedente: [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

 

 
