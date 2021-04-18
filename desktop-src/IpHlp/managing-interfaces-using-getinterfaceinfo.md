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
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Gestione delle interfacce mediante GetInterfaceInfo

La funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) compila un puntatore a una struttura [**di \_ \_ informazioni sull'interfaccia IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con informazioni sulle interfacce associate al sistema.

**Per usare GetInterfaceInfo**

1.  Dichiarare un puntatore a un [**oggetto \_ \_ info dell'interfaccia IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominato `pInfo` e un oggetto **ULONG** denominato `ulOutBufLen` . Dichiarare anche un oggetto **DWORD** denominato `dwRetVal` (usato per il controllo degli errori).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Allocare memoria per le strutture.
    > [!Note]  
    > La dimensione di `ulOutBufLen` non è sufficiente per conservare le informazioni. Vedere il passaggio successivo.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Eseguire una chiamata iniziale a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) per ottenere le dimensioni necessarie nella `ulOutBufLen` variabile.
    > [!Note]  
    > Questa chiamata alla funzione deve avere esito negativo e viene usata per garantire che la `ulOutBufLen` variabile specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a `pInfo` . Si tratta di un modello di programmazione comune nell'helper IP per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Eseguire una seconda chiamata a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con il controllo generale degli errori e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più avanzato).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Se la chiamata ha avuto esito positivo, accedere ai dati dalla `pInfo` struttura dei dati.

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
    > % WS nella prima riga indica una stringa di caratteri "wide". Questa operazione viene utilizzata perché l'attributo **Name** della struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` è un **WCHAR**, ovvero una stringa Unicode.

     

6.  Liberare la memoria allocata per la struttura *pInfo* .
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Passaggio successivo: [gestione degli indirizzi IP con GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Passaggio precedente: [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



