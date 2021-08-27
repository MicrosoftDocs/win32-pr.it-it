---
description: Riempie un puntatore a una struttura FIXED \_ INFO con i dati sulle impostazioni di rete correnti.
ms.assetid: d377951f-e7d4-4482-9182-2c3b153cb325
title: Recupero di informazioni tramite GetNetworkParams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bbe1d03cd619af3a6e73e7995876431a804b3ec723cf9a132df5dba517e719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102040"
---
# <a name="retrieving-information-using-getnetworkparams"></a>Recupero di informazioni tramite GetNetworkParams

La [**funzione GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) riempie un puntatore a una struttura [**FIXED \_ INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) con dati sulle impostazioni di rete correnti.

**Per usare GetNetworkParams**

1.  Dichiarare un puntatore a un [**oggetto FIXED \_ INFO**](/windows/desktop/api/Iptypes/ns-iptypes-fixed_info_w2ksp1) denominato *pFixedInfo* e un **oggetto ULONG** denominato *ulOutBufLen*. Queste variabili vengono passate come parametri alla [**funzione GetNetworkParams.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) Creare anche una **variabile DWORD** *dwRetVal* (usata per il controllo degli errori).
    ```C++
        FIXED_INFO *pFixedInfo;
        IP_ADDR_STRING *pIPAddr;

        ULONG ulOutBufLen;
        DWORD dwRetVal;
    ```

    

2.  Allocare memoria per le strutture.
    > [!Note]  
    > Le dimensioni di *ulOutBufLen* non sono sufficienti per contenere le informazioni. Vedere il passaggio successivo.

     

    ```C++
        pFixedInfo = (FIXED_INFO *) malloc(sizeof (FIXED_INFO));
        ulOutBufLen = sizeof (FIXED_INFO);
    ```

    

3.  Effettuare una chiamata iniziale a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) per ottenere le dimensioni necessarie per la variabile *ulOutBufLen.*
    > [!Note]  
    > Questa funzione avrà esito negativo e viene usata per garantire che la variabile *ulOutBufLen* specifichi una dimensione sufficiente per contenere tutti i dati restituiti a *pFixedInfo*. Si tratta di un modello di programmazione comune per le strutture di dati e le funzioni di questo tipo.

     

    ```C++
        if (GetNetworkParams(pFixedInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
            free(pFixedInfo);
            pFixedInfo = (FIXED_INFO *) malloc(ulOutBufLen);
            if (pFixedInfo == NULL) {
                printf("Error allocating memory needed to call GetNetworkParams\n");
            }
        }
    ```

    

4.  Eseguire una seconda chiamata a [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) usando il controllo degli errori generale e restituire il relativo valore alla variabile **DWORD** *dwRetVal*; usato per il controllo degli errori più avanzato.
    ```C++
        if (dwRetVal = GetNetworkParams(pFixedInfo, &ulOutBufLen) != NO_ERROR) {
            printf("GetNetworkParams failed with error %d\n", dwRetVal);
            if (pFixedInfo) {
                free(pFixedInfo);
            }
        }        
    ```

    

5.  Se la chiamata ha esito positivo, accedere ai dati dalla struttura di dati *pFixedInfo.*
    ```C++
            printf("\tHost Name: %s\n", pFixedInfo->HostName);
            printf("\tDomain Name: %s\n", pFixedInfo->DomainName);
            printf("\tDNS Servers:\n");
            printf("\t\t%s\n", pFixedInfo->DnsServerList.IpAddress.String);

            pIPAddr = pFixedInfo->DnsServerList.Next;
            while (pIPAddr) {
                printf("\t\t%s\n", pIPAddr->IpAddress.String);
                pIPAddr = pIPAddr->Next;
            }

            printf("\tNode Type: ");
            switch (pFixedInfo->NodeType) {
            case 1:
                printf("%s\n", "Broadcast");
                break;
            case 2:
                printf("%s\n", "Peer to peer");
                break;
            case 4:
                printf("%s\n", "Mixed");
                break;
            case 8:
                printf("%s\n", "Hybrid");
                break;
            default:
                printf("\n");
            }

            printf("\tNetBIOS Scope ID: %s\n", pFixedInfo->ScopeId);

            if (pFixedInfo->EnableRouting)
                printf("\tIP Routing Enabled: Yes\n");
            else
                printf("\tIP Routing Enabled: No\n");

            if (pFixedInfo->EnableProxy)
                printf("\tWINS Proxy Enabled: Yes\n");
            else
                printf("\tWINS Proxy Enabled: No\n");

            if (pFixedInfo->EnableDns)
                printf("\tNetBIOS Resolution Uses DNS: Yes\n");
            else
                printf("\tNetBIOS Resolution Uses DNS: No\n");
    ```

    

6.  Liberare la memoria allocata per la *struttura pFixedInfo.*
    ```C++
        if (pFixedInfo) {
            free(pFixedInfo);
            pFixedInfo = NULL;
        }
    ```

    

Passaggio successivo: [Gestione delle schede di rete tramite GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

Passaggio precedente: [Creazione di un'applicazione helper IP di base](creating-a-basic-ip-helper-application.md)

 

 



