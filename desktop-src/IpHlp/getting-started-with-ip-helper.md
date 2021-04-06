---
description: Di seguito è riportata una guida dettagliata per iniziare a programmare con l'helper IP Application Programming Interface (API). È progettato per fornire informazioni sulle funzioni di supporto IP di base e sulle strutture dei dati e sul modo in cui interagiscono.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introduzione con helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885713"
---
# <a name="getting-started-with-ip-helper"></a>Introduzione con helper IP

Di seguito è riportata una guida dettagliata per iniziare a programmare con l'helper IP Application Programming Interface (API). È progettato per fornire informazioni sulle funzioni di supporto IP di base e sulle strutture dei dati e sul modo in cui interagiscono.

L'applicazione usata per l'illustrazione è un'applicazione helper IP di base. Negli esempi inclusi nel Software Development Kit (SDK) di Microsoft Windows sono inclusi esempi di codice più avanzati.

Il primo passaggio è identico per la maggior parte delle applicazioni helper IP.

-   [Creazione di un'applicazione helper IP di base](creating-a-basic-ip-helper-application.md)

Le sezioni seguenti descrivono i passaggi rimanenti per la creazione di questa applicazione helper IP di base.

-   [Recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Gestione delle interfacce mediante GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Gestione degli indirizzi IP tramite GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Gestione degli indirizzi IP con AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Recupero di informazioni tramite GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Recupero di informazioni tramite GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Il codice sorgente completo per questo esempio di helper IP di base.

-   [Codice sorgente completo dell'applicazione helper IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Esempi avanzati di helper IP

Con Microsoft Windows Software Development Kit (SDK) sono inclusi diversi esempi di helper IP più avanzati. Per impostazione predefinita, il codice sorgente di esempio dell'helper IP viene installato dalla Windows SDK rilasciata per Windows 7 nella seguente directory:

*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ IPHelp*

Gli esempi più avanzati elencati di seguito sono disponibili nelle directory seguenti:

-   EnableRouter

    Questa directory contiene un esempio che illustra come usare le funzioni di supporto IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) e [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) per abilitare e disabilitare l'invio IPv4 nel computer locale.

-   iparp

    Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per visualizzare e modificare le voci nella tabella ARP IPv4 nel computer locale.

-   ipchange

    Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per modificare a livello di codice un indirizzo IP per una scheda di rete specifica nel computer. Questo programma illustra anche come recuperare le informazioni di configurazione IP della scheda di rete esistente.

-   IPConfig

    Questa directory contiene un programma di esempio che illustra come recuperare a livello di codice le informazioni di configurazione IPv4 simili all'utilità IPCONFIG.EXE. Viene illustrato come usare le funzioni [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) e [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) . Si noti che la funzione **GetAdaptersInfo** recupera solo le informazioni IPv4.

-   IPRenew

    Questa directory contiene un programma di esempio in cui viene illustrato come rilasciare e rinnovare gli indirizzi IPv4 ottenuti tramite DHCP a livello di codice. Questo programma illustra anche come recuperare le informazioni di configurazione delle schede di rete esistenti.

-   IPRoute

    Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per modificare la tabella di routing IPv4.

-   ipstat

    Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per visualizzare le connessioni IPv4 per un protocollo. Per impostazione predefinita, vengono visualizzate le statistiche per IP, ICMP, TCP e UDP.

-   NetInfo

    Questa directory contiene un programma di esempio che illustra come usare le nuove API helper IP introdotte in Windows Vista e versioni successive per visualizzare/modificare le informazioni sull'indirizzo e sull'interfaccia per IPv4 e IPv6.

 

 



