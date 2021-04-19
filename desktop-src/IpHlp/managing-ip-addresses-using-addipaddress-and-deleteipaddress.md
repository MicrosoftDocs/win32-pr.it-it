---
title: Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress
description: La funzione AddIPAddress aggiunge l'indirizzo IPv4 specificato all'adapter specificato.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311751"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a>Gestire gli indirizzi IP con AddIPAddress, DeleteIPAddress

La funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) aggiunge l'indirizzo IPv4 specificato all'adapter specificato. La funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) Elimina l'indirizzo IPv4 specificato dall'adapter specificato. Queste funzioni possono essere utilizzate per aggiungere ed eliminare indirizzi IPv4 a una scheda di rete.

Un indirizzo IPv4 aggiunto dalla funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) non è persistente. L'indirizzo IPv4 esiste solo fino a quando l'oggetto adapter esiste. Il riavvio del computer comporta l'eliminazione dell'indirizzo IPv4, così come si ripristina manualmente la scheda di interfaccia di rete (NIC).

Dopo che [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) è stato chiamato correttamente, DHCP verrà disabilitato per l'indirizzo IP aggiunto. Pertanto, le funzioni come [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), che richiedono l'abilitazione di DHCP, non funzioneranno sull'indirizzo IP aggiunto. Per eliminare l'indirizzo IPv4 aggiunto, è possibile utilizzare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) .

> [!Note]  
> Criteri di gruppo, criteri aziendali e altre restrizioni sulla rete possono impedire il corretto completamento di queste funzioni. Assicurarsi che l'applicazione disponga delle autorizzazioni di rete necessarie prima di provare a usare queste funzioni.

 

**Per usare AddIPAddress**

1.  Dichiarare le variabili **ULONG** denominate `NTEContext` e `NTEInstance` , entrambe inizializzate su zero.
    > [!Note]  
    > La `NTEContext` variabile è l'unico parametro per la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) . per eliminare l'indirizzo IP aggiunto, `NTEContext` deve essere archiviato e non modificato.

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  Dichiarare le variabili per le strutture IPAddr e IPMask denominate `iaIPAddress` `iaIPMask` rispettivamente e. Questi valori sono semplicemente interi senza segno. Inizializzare `iaIPAddress` le `iaIPMask` variabili e mediante la funzione [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) .
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  Chiamare la funzione [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per aggiungere l'indirizzo IPv4. Verificare la presenza di errori e restituire il valore di errore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > Il terzo parametro è l'indice dell'adattatore, che può essere ottenuto chiamando la funzione [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) . Si presuppone che la variabile restituita da questa funzione sia denominata `pIPAddrTable` . Per informazioni sulla funzione **GetIpAddrTable** , vedere [Managing IP address using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).

     

**Per usare DeleteIpAddress**

-   Chiamare la funzione [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) , passando la `NTEContext` variabile come parametro. Verificare la presenza di errori e restituire il valore di errore alla variabile **DWORD** `dwRetVal` (per un controllo degli errori più completo).
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> Per usare [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), è prima necessario chiamare [**AddIpAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) per ottenere l'handle `NTEContext` . Nella procedura precedente si presuppone che **AddIpAddress** sia già stato chiamato in un punto qualsiasi del codice ed `NTEContext` è stato salvato e rimane inalterato.

 

Passaggio successivo: [recupero di informazioni tramite GetIPStatistics](retrieving-information-using-getipstatistics.md)

Passaggio precedente: [gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)

 

 
