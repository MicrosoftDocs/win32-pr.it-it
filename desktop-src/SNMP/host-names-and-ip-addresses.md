---
title: Nomi host e indirizzi IP
description: Le reti TCP/IP richiedono che i nomi host siano risolti in indirizzi IP prima che le informazioni sull'indirizzo possano essere usate per creare una connessione.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Nomi host e indirizzi IP SNMP
- Nomi host, risoluzione di SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009509"
---
# <a name="host-names-and-ip-addresses"></a>Nomi host e indirizzi IP

Le reti TCP/IP richiedono che i nomi host siano risolti in indirizzi IP prima che le informazioni sull'indirizzo possano essere usate per creare una connessione. I computer in esecuzione Windows sistema operativo usano un file host che, a questo scopo, esegue il mapping dei nomi host agli indirizzi IP.

Il file host è un file di testo che elenca nomi host e indirizzi IP espliciti. Il file host viene caricato automaticamente in memoria all'avvio e consultato quando un nome host richiede la risoluzione. Se il file host non contiene le informazioni di mapping necessarie per risolvere un nome host specifico nel relativo indirizzo IP, viene eseguita una query di risoluzione in un server DNS.

SNMP usa il Windows Internet Naming Service (WINS) per la risoluzione dei nomi host. WINS consente di eseguire il mapping dei nomi NetBIOS, o nomi di computer, agli indirizzi IP nelle reti TCP/IP. Se il computer non può accedere a un server WINS, il servizio SNMP usa il file host per risolvere i nomi host in indirizzi IP.

Il servizio SNMP supporta l'uso di nomi host e indirizzi IP. Tuttavia, quando è possibile scegliere tra l'uso di nomi host o indirizzi IP per identificare i percorsi di rete, le applicazioni di gestione SNMP devono usare i nomi host. Se si usano nomi host, aggiungere tutti i mapping di nomi host e indirizzi IP dei sistemi partecipanti al file host.

 

 




