---
title: Nomi host e indirizzi IP
description: Le reti TCP/IP richiedono la risoluzione dei nomi host negli indirizzi IP prima che sia possibile utilizzare le informazioni sull'indirizzo per creare una connessione.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Indirizzi IP e nomi host SNMP
- Nomi host, risoluzione SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709580"
---
# <a name="host-names-and-ip-addresses"></a>Nomi host e indirizzi IP

Le reti TCP/IP richiedono la risoluzione dei nomi host negli indirizzi IP prima che sia possibile utilizzare le informazioni sull'indirizzo per creare una connessione. Nei computer che eseguono il sistema operativo Windows viene utilizzato un file host che, a tale scopo, esegue il mapping dei nomi host agli indirizzi IP.

Il file host è un file di testo in cui sono elencati i nomi host e gli indirizzi IP espliciti. Il file host viene caricato automaticamente in memoria all'avvio e viene consultato quando è necessario risolvere un nome host. Se il file host non contiene le informazioni di mapping necessarie per risolvere un nome host specifico nel relativo indirizzo IP, viene eseguita una query di risoluzione su un server DNS.

SNMP usa Windows Internet Naming Service (WINS) per la risoluzione dei nomi host. WINS consente di eseguire il mapping di nomi NetBIOS o nomi di computer a indirizzi IP su reti TCP/IP. Se il computer non è in grado di accedere a un server WINS, il servizio SNMP utilizza il file host per risolvere i nomi host in indirizzi IP.

Il servizio SNMP supporta l'utilizzo di nomi host e indirizzi IP. Tuttavia, quando è possibile scegliere tra l'utilizzo di nomi host o indirizzi IP per identificare i percorsi di rete, le applicazioni di gestione SNMP devono utilizzare nomi host. Se si utilizzano nomi host, aggiungere tutti i mapping di nome host e indirizzo IP dei sistemi partecipanti al file host.

 

 




