---
title: Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress
description: La funzione AddIPAddress aggiunge l'indirizzo IPv4 specificato all'adapter specificato.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e726a2e5785641532abb739d61143f9fabfdd10c38e4b51fcd529f20d92503d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870091"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress

La [**funzione AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) aggiunge l'indirizzo IPv4 specificato all'adapter specificato. La [**funzione DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) elimina l'indirizzo IPv4 specificato dall'adapter specificato. Queste funzioni possono essere usate per aggiungere ed eliminare indirizzi IPv4 a una scheda di rete.

Un indirizzo IPv4 aggiunto dalla [**funzione AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) non è persistente. L'indirizzo IPv4 esiste solo se l'oggetto adapter esiste. Il riavvio del computer elimina l'indirizzo IPv4, così come la reimpostazione manuale della scheda di interfaccia di rete .

Dopo [**che AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) è stato chiamato correttamente, DHCP verrà disabilitato per l'indirizzo IP aggiunto. Pertanto, funzioni come [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), che richiedono l'a attivazione di DHCP, non saranno funzionali nell'indirizzo IP aggiunto. La [**funzione DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) può essere usata per eliminare l'indirizzo IPv4 aggiunto.

> [!Note]  
> I criteri di gruppo, i criteri aziendali e altre restrizioni nella rete possono impedire il corretto completamento di queste funzioni. Assicurarsi che l'applicazione abbia le autorizzazioni di rete necessarie prima di provare a usare queste funzioni.

 

**Per usare AddIPAddress**

1.  Dichiarare **le variabili ULONG** `NTEContext` denominate e , `NTEInstance` entrambe inizializzate su zero.
    > [!Note]  
    > La `NTEContext` variabile è l'unico parametro della funzione [**DeleteIPAddress.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) Per eliminare l'indirizzo IP aggiunto, deve `NTEContext` essere archiviato e invariato.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Dichiarare variabili per le strutture IPAddr e IPMask denominate `iaIPAddress` `iaIPMask` rispettivamente e . Questi valori sono semplicemente interi senza segno. Inizializzare `iaIPAddress` le variabili e usando la funzione `iaIPMask` [**\_ addr inet.**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Chiamare la [**funzione AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere l'indirizzo IPv4. Verificare la presenza di errori e restituire il valore di errore alla **variabile DWORD** `dwRetVal` (per un controllo degli errori più completo).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Il terzo parametro è l'indice dell'adapter, che può essere ottenuto chiamando la [**funzione GetIpAddrTable.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) Si presuppone che la variabile restituita da questa funzione sia denominata `pIPAddrTable` . Per informazioni sulla **funzione GetIpAddrTable,** vedere [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Per usare DeleteIpAddress**

-   Chiamare la [**funzione DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) passando `NTEContext` la variabile come parametro. Verificare la presenza di errori e restituire il valore di errore alla **variabile DWORD** `dwRetVal` (per un controllo degli errori più completo).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Per usare [**DeleteIPAddress,**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)è prima necessario chiamare [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per ottenere l'handle `NTEContext` . La procedura precedente presuppone che **AddIPAddress** sia già stato chiamato in un punto qualsiasi del codice ed è stato salvato e rimane `NTEContext` incorretta.

 

Passaggio successivo: [Recupero di informazioni tramite GetIpStatistics](retrieving-information-using-getipstatistics.md)

Passaggio precedente: [Gestione dei lease DHCP tramite IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
