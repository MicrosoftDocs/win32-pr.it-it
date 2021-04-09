---
title: Gestire lease DHCP con IpReleaseAddress, IpRenewAddress
description: Le funzioni IpReleaseAddress e IpRenewAddress vengono utilizzate per rilasciare e rinnovare il lease del Dynamic Host Configuration Protocol corrente (DHCP).
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879082"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a>Gestire lease DHCP con IpReleaseAddress, IpRenewAddress

Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) vengono utilizzate per rilasciare e rinnovare il lease del Dynamic Host Configuration Protocol corrente (DHCP). La funzione **IpReleaseAddress** rilascia un indirizzo IPv4 ottenuto in precedenza tramite DHCP. La funzione **IpRenewAddress** rinnova un lease in un indirizzo IPv4 ottenuto in precedenza tramite DHCP. È comune usare queste due funzioni insieme, per prima cosa rilasciare il lease con una chiamata a **IpReleaseAddress** e quindi rinnovare il lease con una chiamata alla funzione **IpRenewAddress** .

Quando un client DHCP ha ottenuto in precedenza un lease DHCP e [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) non viene chiamato prima della funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , la richiesta del client DHCP viene inviata al server DHCP che ha emesso il lease DHCP iniziale. Questo server DHCP potrebbe non essere disponibile o la richiesta DHCP potrebbe non riuscire. Quando un host ha ottenuto in precedenza un lease DHCP e **IpReleaseAddress** viene chiamato prima della funzione **IpRenewAddress** , il client DHCP rilascia innanzitutto l'indirizzo IP ottenuto e invia una richiesta del client DHCP per una risposta da qualsiasi server DHCP disponibile.

> [!Note]  
> Le funzioni [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e [**IPRENEWADDRESS**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) richiedono che DHCP sia abilitato per una corretta esecuzione.

 

La funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) accetta un puntatore a una struttura della mappa dell' [**indice della \_ scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) come unico parametro. Per ottenere questo parametro, chiamare prima [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo). Per informazioni sulla funzione **GetInterfaceInfo** , vedere [gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).

**Per usare IpReleaseAddress**

1.  Ottenere un puntatore a una struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) utilizzando la funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . Per informazioni sulla funzione GetInterfaceInfo, vedere Gestione delle [interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md). Creare un  oggetto DWORD `dwRetVal` (usato per il controllo degli errori). Si presuppone che venga chiamata la variabile restituita da **GetInterfaceInfo** `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Se DHCP è abilitato, chiamare la funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) , passando la variabile della mappa dell' [**\_ \_ indice \_ della scheda IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` come parametro. Verificare la presenza di errori generali e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).
    > [!Note]  
    > La funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) restituisce un parametro che può essere utilizzato per verificare se DHCP è abilitato prima di chiamare queste funzioni. Per informazioni su **GetAdaptersInfo**, vedere [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> È comune usare queste due funzioni insieme, chiamando la funzione [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) e quindi chiamando la funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando la stessa struttura del parametro a entrambe le funzioni. Nella procedura seguente si presuppone che le funzioni non vengano utilizzate insieme; Tuttavia, se le funzioni vengono utilizzate insieme, ignorare il passaggio 1.

 

**Per usare IpRenewAddress**

1.  Ottenere un puntatore a una struttura della [**mappa dell' \_ indice della scheda \_ \_ IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) utilizzando la funzione [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) . Per informazioni sulla funzione **GetInterfaceInfo** , vedere Gestione delle [interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md). Dichiarare un  oggetto DWORD `dwRetVal` (usato per il controllo degli errori) se questa variabile non è stata dichiarata. Si presuppone che venga chiamata la variabile restituita da **GetInterfaceInfo** `pInfo` .
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  Chiamare la funzione [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) , passando la variabile della mappa dell' [**\_ \_ indice \_ dell'adattatore IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` come parametro. Verificare la presenza di errori generali e restituirne il valore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

Passaggio successivo: [gestione degli indirizzi IP con AddIpAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)

Passaggio precedente: [gestione degli indirizzi IP con GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

 

 



