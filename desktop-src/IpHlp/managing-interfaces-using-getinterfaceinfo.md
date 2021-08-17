---
description: La funzione GetInterfaceInfo riempie un puntatore a una struttura IP INTERFACE INFO con informazioni sulle \_ \_ interfacce associate al sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gestione delle interfacce tramite GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2afa6fe0b520e1cc5f952b44bc94052b630f4335bd739b4d7c3582d16e277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146744"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Gestione delle interfacce tramite GetInterfaceInfo

La [**funzione GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) riempie un puntatore a una struttura [**IP INTERFACE \_ \_ INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) con informazioni sulle interfacce associate al sistema.

**Per usare GetInterfaceInfo**

1.  Dichiarare un puntatore a [**un oggetto IP INTERFACE \_ \_ INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) denominato `pInfo` e un oggetto **ULONG** denominato `ulOutBufLen` . Dichiarare anche un **oggetto DWORD** denominato `dwRetVal` (usato per il controllo degli errori).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Allocare memoria per le strutture.
    > [!Note]  
    > Le dimensioni di `ulOutBufLen` non sono sufficienti per contenere le informazioni. Vedere il passaggio successivo.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Effettuare una chiamata iniziale a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) per ottenere le dimensioni necessarie nella `ulOutBufLen` variabile.
    > [!Note]  
    > Questa chiamata alla funzione ha esito negativo e viene usata per garantire che la variabile specifichi una dimensione sufficiente per contenere tutte le `ulOutBufLen` informazioni restituite a `pInfo` . Si tratta di un modello di programmazione comune nell'helper IP per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Eseguire una seconda chiamata a [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) con il controllo degli errori generale e restituirne il valore alla **variabile DWORD** `dwRetVal` (per un controllo degli errori più avanzato).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Se la chiamata ha esito positivo, accedere ai dati dalla `pInfo` struttura dei dati.

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
    > %ws nella prima riga indica una stringa wide. Viene usato perché **l'attributo Name** della struttura [**IP ADAPTER INDEX \_ \_ \_ MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` è un **WCHAR,** ovvero una stringa Unicode.

     

6.  Liberare la memoria allocata per la *struttura pInfo.*
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Passaggio successivo: [Gestione degli indirizzi IP tramite GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Passaggio precedente: [Gestione delle schede di rete tramite GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



