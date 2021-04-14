---
description: Come creare un'applicazione helper IP di base.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Creazione di un'applicazione helper IP di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350266"
---
# <a name="creating-a-basic-ip-helper-application"></a>Creazione di un'applicazione helper IP di base

**Per creare un'applicazione helper IP di base**

1.  Creare un nuovo progetto vuoto.
2.  Aggiungere un file di origine C++ vuoto al progetto.
3.  Verificare che l'ambiente di compilazione faccia riferimento alle directory include, lib e src di Platform Software Development Kit (SDK).
4.  Verificare che l'ambiente di compilazione sia collegato al file della libreria helper IP iphlpapi. lib e al file della libreria WinSock WS2 \_ 32. lib.
    > [!Note]  
    > Alcune funzioni Winsock di base vengono utilizzate per restituire i valori degli indirizzi IP e altre informazioni.

     

5.  Iniziare a programmare l'applicazione helper IP. Usare l'API helper IP includendo il file di intestazione dell'helper IP.

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Il file di intestazione *iphlpapi. h* è necessario per le applicazioni che usano le funzioni di supporto IP. Il file di intestazione *iphlpapi. h* include automaticamente altri file di intestazioni con strutture ed enumerazioni usate dalle funzioni helper IP.
    >
    > Le nuove funzioni helper IP introdotte in Windows Vista e versioni successive sono definite nel file di intestazione *Netioapi. h* , incluso automaticamente nel file di intestazione *iphlpapi. h* . Il file di intestazione *Netioapi. h* non deve mai essere utilizzato direttamente.
    >
    > Molte strutture ed enumerazioni usate dalle funzioni helper IP sono definite nei file di intestazione *Iprtrmib. h*, *Ipexport. h* e *Iptypes. h* . Questi file di intestazione vengono inclusi automaticamente nel file di intestazione *iphlpapi. h* e non devono mai essere usati direttamente.
    >
    > In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è cambiata. Alcune strutture sono ora definite nei file di intestazione *Ipmib. h*, *tcpmib. h* e *Udpmib. h* , non nel file di intestazione *Iprtrmib. h* . Il file di intestazione *Ipmib. h* include automaticamente il file di intestazione *ifmib. h* . Si noti che questi file di intestazione vengono inclusi automaticamente in *Iprtrmib. h*, che viene automaticamente incluso nel file di intestazione *iphlpapi. h* .
    >
    > Il file di intestazione *Winsock2. h* per Windows sockets 2,0 è richiesto dalla maggior parte delle applicazioni che usano le API helper IP. Quando il file di intestazione *Winsock2. h* è obbligatorio, la \# riga di inclusione per questo file deve essere posizionata prima della \# riga di inclusione per il file di intestazione *iphlpapi. h* .
    >
    > Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione *Windows. h* nelle applicazioni helper IP. Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ . Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1. Le dichiarazioni nel file di intestazione *Winsock. h* per Windows sockets 1,1 sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2,0. La \_ macro Win32 snello \_ e \_ media impedisce che il file di intestazione *Winsock. h* venga incluso nel file di intestazione di *Windows. h* . Di seguito è riportato un esempio che illustra questo problema.

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Questa applicazione helper IP di base usa solo alcune strutture di dati degli indirizzi IP e l'indirizzo IP per le funzioni di conversione di stringhe da Windows Sockets 2,0. Queste funzioni di Windows Sockets possono essere utilizzate senza chiamare [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare le risorse di Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando vengono eseguite utilizzando queste risorse.
    >
    > Nelle applicazioni helper IP che usano altre funzioni Winsock diverse da questo indirizzo IP alle funzioni di stringa, è necessario chiamare la funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare le risorse di Windows Sockets prima di chiamare qualsiasi funzione Windows Sockets ed è necessario chiamare [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando l'applicazione viene eseguita usando le risorse di Windows Sockets.

     

    > [!Note]
    >
    > Il file di intestazione *stdio. h* è necessario per l'uso di varie funzioni C standard in questa applicazione helper IP di base.

     

    Passaggio successivo: [recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)

 

 
