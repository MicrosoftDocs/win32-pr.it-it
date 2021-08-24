---
description: La funzione GetIpAddrTable riempie un puntatore a una struttura MIB IPADDRTABLE con informazioni sugli indirizzi IP correnti \_ associati al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gestione degli indirizzi IP tramite GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090bdb1e73d3f770eafb3a5e70893253918eb68573ebd05aa6ec40a609a7ba4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146684"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Gestione degli indirizzi IP tramite GetIpAddrTable

La [**funzione GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) riempie un puntatore a una struttura [**\_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) con informazioni sugli indirizzi IP correnti associati al sistema.

**Per usare GetIpAddrTable**

1.  Dichiarare un puntatore a [**un oggetto \_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) denominato *pIPAddrTable* e un **oggetto DWORD** denominato *dwSize*. Queste variabili vengono passate come parametri alla [**funzione GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Creare anche una **variabile DWORD** denominata *dwRetVal* (usata per il controllo degli errori).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Allocare memoria per la struttura.
    > [!Note]  
    > Le dimensioni di *dwSize* non sono sufficienti per contenere le informazioni. Vedere il passaggio successivo.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Eseguire una chiamata iniziale a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) per ottenere le dimensioni necessarie nella *variabile dwSize.*
    > [!Note]  
    > Questa chiamata alla funzione ha esito negativo e viene usata per garantire che la *variabile dwSize* specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a *pIPAddrTable*. Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Eseguire una seconda chiamata a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con il controllo degli errori generale e restituire il relativo valore alla variabile **DWORD** *dwRetVal* (per un controllo degli errori più avanzato).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Se la chiamata ha esito positivo, accedere ai dati dalla struttura di dati *pIPAddrTable.*
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Liberare la memoria allocata per la *struttura pIPAddrTable.*
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Gli **oggetti DWORD** *dwAddr* e *dwMask* vengono restituiti come valori numerici nell'ordine dei byte dell'host, non come ordine dei byte di rete. Questi valori non sono indirizzi IP punteggiati.

 

Passaggio successivo: [Gestione dei lease DHCP tramite IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Passaggio precedente: [Gestione delle interfacce tramite GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
