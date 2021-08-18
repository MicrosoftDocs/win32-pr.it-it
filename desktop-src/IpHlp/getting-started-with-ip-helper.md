---
description: Di seguito è riportata una guida dettagliata per iniziare a programmare usando l'API (Application Programming Interface) dell'helper IP. È progettato per offrire una conoscenza delle funzioni di base dell'helper IP e delle strutture dei dati e del modo in cui funzionano insieme.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Attività iniziali con l'helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ca2df12a7d2d2cbd2d0a64f1da07c8aeecd4980fea791bfc19ca018cd87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014159"
---
# <a name="getting-started-with-ip-helper"></a>Attività iniziali con l'helper IP

Di seguito è riportata una guida dettagliata per iniziare a programmare usando l'API (Application Programming Interface) dell'helper IP. È progettato per offrire una conoscenza delle funzioni di base dell'helper IP e delle strutture dei dati e del modo in cui funzionano insieme.

L'applicazione usata a scopo illustrativo è un'applicazione helper IP molto semplice. Esempi di codice più avanzati sono inclusi negli esempi inclusi in Microsoft Windows Software Development Kit (SDK).

Il primo passaggio è lo stesso per la maggior parte delle applicazioni helper IP.

-   [Creazione di un'applicazione helper IP di base](creating-a-basic-ip-helper-application.md)

Le sezioni seguenti descrivono i passaggi rimanenti per la creazione di questa applicazione helper IP di base.

-   [Recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)
-   [Gestione delle schede di rete tramite GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)
-   [Gestione delle interfacce tramite GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)
-   [Gestione degli indirizzi IP tramite GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)
-   [Gestione dei lease DHCP tramite IpReleaseAddress e IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [Gestione degli indirizzi IP tramite AddIPAddress e DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [Recupero di informazioni tramite GetIpStatistics](retrieving-information-using-getipstatistics.md)
-   [Recupero di informazioni tramite GetTcpStatistics](retrieving-information-using-gettcpstatistics.md)

Codice sorgente completo per questo esempio di helper IP di base.

-   [Codice sorgente completo dell'applicazione helper IP](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a>Esempi avanzati di helper IP

In Microsoft Windows Software Development Kit (SDK) sono inclusi diversi esempi di helper IP più avanzati. Per impostazione predefinita, il codice sorgente di esempio dell'helper IP viene installato da Windows SDK rilasciato per Windows 7 nella directory seguente:

*C: \\ Programmi \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples \\ NetDs \\ IPHelp*

Gli esempi più avanzati elencati di seguito sono disponibili nelle directory seguenti:

-   EnableRouter

    Questa directory contiene un esempio che illustra come usare le funzioni [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) e [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper per abilitare e disabilitare l'inoltro IPv4 nel computer locale.

-   iparp

    Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per visualizzare e modificare le voci nella tabella ARP IPv4 nel computer locale.

-   ipchange

    Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per modificare a livello di codice un indirizzo IP per una scheda di rete specifica nel computer. Questo programma illustra anche come recuperare le informazioni di configurazione IP della scheda di rete esistente.

-   IPConfig

    Questa directory contiene un programma di esempio che illustra come recuperare a livello di codice informazioni di configurazione IPv4 simili all'IPCONFIG.EXE predefinita. Illustra come usare le [**funzioni GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) [**e GetAdaptersInfo.**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) Si noti che **la funzione GetAdaptersInfo** recupera solo le informazioni IPv4.

-   NUOVO INDIRIZZO IP

    Questa directory contiene un programma di esempio che illustra come rilasciare e rinnovare a livello di codice gli indirizzi IPv4 ottenuti tramite DHCP. Questo programma illustra anche come recuperare le informazioni di configurazione della scheda di rete esistente.

-   IPRoute

    Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per modificare la tabella di routing IPv4.

-   ipstat

    Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per visualizzare le connessioni IPv4 per un protocollo. Per impostazione predefinita, vengono visualizzate le statistiche per IP, ICMP, TCP e UDP.

-   Netinfo

    Questa directory contiene un programma di esempio che illustra come usare le nuove API helper IP introdotte in Windows Vista e versioni successive per visualizzare/modificare le informazioni sull'indirizzo e sull'interfaccia per IPv4 e IPv6.

 

 



