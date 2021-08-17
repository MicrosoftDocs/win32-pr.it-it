---
description: La funzione GetAdaptersInfo riempie un puntatore a una struttura IP ADAPTER INFO con informazioni sulle schede di \_ \_ rete associate al sistema.
ms.assetid: 5bc72ee5-3065-4bfb-8dcb-8befb2a4bbd9
title: Gestione delle schede di rete tramite GetAdaptersInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da19541572af89e9429b9deba68efd4f4670324ffd9ff824e6c123295108f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644631"
---
# <a name="managing-network-adapters-using-getadaptersinfo"></a>Gestione delle schede di rete tramite GetAdaptersInfo

La [**funzione GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) riempie un puntatore a una struttura [**IP ADAPTER \_ \_ INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) con informazioni sulle schede di rete associate al sistema.

**Per usare GetAdaptersInfo**

1.  Dichiarare un puntatore a [**una variabile IP ADAPTER \_ \_ INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) denominata *pAdapterInfo* e una variabile **ULONG** denominata *ulOutBufLen*. Queste variabili vengono passate come parametri alla [**funzione GetAdaptersInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) Creare anche una **variabile DWORD** denominata *dwRetVal* (per il controllo degli errori).
    ```C++
    IP_ADAPTER_INFO  *pAdapterInfo;
    ULONG            ulOutBufLen;
    DWORD            dwRetVal;
    
    ```

    

2.  Allocare memoria per le strutture.
    ```C++
    pAdapterInfo = (IP_ADAPTER_INFO *) malloc( sizeof(IP_ADAPTER_INFO) );
    ulOutBufLen = sizeof(IP_ADAPTER_INFO);
    
    ```

    

3.  Effettuare una chiamata iniziale a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) per ottenere le dimensioni necessarie nella variabile *ulOutBufLen.*
    > [!Note]  
    > Questa chiamata alla funzione ha esito negativo e viene usata per garantire che la variabile *ulOutBufLen* specifichi una dimensione sufficiente per contenere tutte le informazioni restituite a *pAdapterInfo*. Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
    if (GetAdaptersInfo( pAdapterInfo, &ulOutBufLen) != ERROR_SUCCESS) {
        free (pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) malloc ( ulOutBufLen );
    }
    
    ```

    

4.  Effettuare una seconda chiamata a [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo), passando *pAdapterInfo* e *ulOutBufLen* come parametri ed eseguendo il controllo degli errori generale. Restituire il valore alla **variabile DWORD** *dwRetVal* (per un controllo degli errori più completo).
    ```C++
    if ((dwRetVal = GetAdaptersInfo( pAdapterInfo, &ulOutBufLen)) != ERROR_SUCCESS) {
        printf("GetAdaptersInfo call failed with %d\n", dwRetVal);
    }

    
    ```

    

5.  Se la chiamata ha esito positivo, accedere ad alcuni dei dati nella *struttura pAdapterInfo.*
    ```C++
    PIP_ADAPTER_INFO pAdapter = pAdapterInfo;
    while (pAdapter) {
        printf("Adapter Name: %s\n", pAdapter->AdapterName);
        printf("Adapter Desc: %s\n", pAdapter->Description);
        printf("\tAdapter Addr: \t");
        for (UINT i = 0; i < pAdapter->AddressLength; i++) {
            if (i == (pAdapter->AddressLength - 1))
                printf("%.2X\n",(int)pAdapter->Address[i]);
            else
                printf("%.2X-",(int)pAdapter->Address[i]);
        }
        printf("IP Address: %s\n", pAdapter->IpAddressList.IpAddress.String);
        printf("IP Mask: %s\n", pAdapter->IpAddressList.IpMask.String);
        printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
        printf("\t***\n");
        if (pAdapter->DhcpEnabled) {
            printf("\tDHCP Enabled: Yes\n");
            printf("\t\tDHCP Server: \t%s\n", pAdapter->DhcpServer.IpAddress.String);
        }
        else
          printf("\tDHCP Enabled: No\n");

      pAdapter = pAdapter->Next;
    }
    
    ```

    

6.  Liberare la memoria allocata per la *struttura pAdapterInfo.*
    ```C++
    if (pAdapterInfo)
            free(pAdapterInfo);
    
    ```

    

Passaggio successivo: [Gestione delle interfacce tramite GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)

Passaggio precedente: [Recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 



