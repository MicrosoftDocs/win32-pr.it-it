---
description: La funzione GetIpAddrTable compila un puntatore a una \_ struttura IPADDRTABLE MIB con informazioni sugli indirizzi IP correnti associati al sistema.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Gestione degli indirizzi IP tramite GetIpAddrTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881518"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a>Gestione degli indirizzi IP tramite GetIpAddrTable

La funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) compila un puntatore a una struttura [**\_ IPADDRTABLE MIB**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) con informazioni sugli indirizzi IP correnti associati al sistema.

**Per usare GetIpAddrTable**

1.  Dichiarare un puntatore a un [**oggetto \_ MIB IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) denominato *PIPAddrTable* e un oggetto **DWORD** denominato *dwSize*. Queste variabili vengono passate come parametri alla funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Creare anche una variabile **DWORD** denominata *dwRetVal* (usata per il controllo degli errori).
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  Allocare memoria per la struttura.
    > [!Note]  
    > Le dimensioni di *dwSize* non sono sufficienti per conservare le informazioni. Vedere il passaggio successivo.

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  Eseguire una chiamata iniziale a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) per ottenere le dimensioni necessarie nella variabile *dwSize* .
    > [!Note]  
    > Questa chiamata alla funzione deve avere esito negativo e viene usata per garantire che la variabile *dwSize* specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a *pIPAddrTable*. Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  Eseguire una seconda chiamata a [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) con il controllo generale degli errori e restituirne il valore alla variabile **DWORD** *dwRetVal* (per un controllo degli errori più avanzato).
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  Se la chiamata ha avuto esito positivo, accedere ai dati dalla struttura di dati *pIPAddrTable* .
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  Liberare la memoria allocata per la struttura *pIPAddrTable* .
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> Gli  oggetti DWORD *dwAddr* e *dwMask* vengono restituiti come valori numerici nell'ordine dei byte dell'host, non nell'ordine dei byte di rete. Questi valori non sono indirizzi IP punteggiati.

 

Passaggio successivo: [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

Passaggio precedente: [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

 

 
