---
title: Funzioni server (gestione di rete)
description: Le funzioni del server di gestione di rete eseguono attività amministrative in un server locale o remoto. Le funzioni server sono elencate di seguito.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086abbd23682c17bb1bbfee6180067ca0947a848a4a8dfadb36ba1b87ef13c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983135"
---
# <a name="server-functions-network-management"></a>Funzioni server (gestione di rete)

Le funzioni del server di gestione di rete eseguono attività amministrative in un server locale o remoto. Le funzioni server sono elencate di seguito.



| Funzione                                       | Descrizione                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Restituisce un elenco di unità disco locali in un server.                                   |
| [**Enumerazione NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Elenca tutti i server visibili di un particolare tipo (o tipi) nel dominio specificato. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Restituisce informazioni di configurazione su un server specificato.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Imposta i parametri operativi per un server.                                        |



 

Solo un utente o un'applicazione con appartenenza a un gruppo amministrativo in un server locale o remoto può eseguire attività amministrative su tale server per controllare il funzionamento del server, l'accesso utente e la condivisione delle risorse. I parametri di basso livello che influiscono sull'operazione di un server possono essere esaminati e modificati chiamando le funzioni [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo.**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) Questi parametri sono definiti nel file LANMAN.INI server.

La maggior parte delle funzioni del server di gestione di rete viene eseguita solo in un server remoto. La [**funzione NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) viene eseguita in una workstation locale o in un server remoto. Se si tenta di eseguire altre funzioni server in una workstation locale, le funzioni restituiscono l'errore NERR \_ RemoteOnly.

Le informazioni specifiche del server sono disponibili ai livelli seguenti:

-   [**INFORMAZIONI \_ SERVER \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**INFORMAZIONI \_ SERVER \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**INFORMAZIONI \_ SERVER \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**INFORMAZIONI \_ SERVER \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**INFORMAZIONI \_ SERVER \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**INFORMAZIONI \_ SERVER \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**INFORMAZIONI \_ SERVER \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**INFORMAZIONI \_ SERVER \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**INFORMAZIONI \_ SERVER \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**INFORMAZIONI \_ SERVER \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**INFORMAZIONI \_ SERVER \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**INFORMAZIONI \_ SERVER \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**INFORMAZIONI \_ SERVER \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**INFORMAZIONI \_ SERVER \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**INFORMAZIONI \_ SERVER \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**INFORMAZIONI \_ SERVER \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**INFORMAZIONI \_ SERVER \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**INFORMAZIONI \_ SERVER \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**INFORMAZIONI \_ SERVER \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**INFORMAZIONI \_ SERVER \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**INFORMAZIONI \_ SERVER \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**INFORMAZIONI \_ SERVER \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**INFORMAZIONI \_ SERVER \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**INFORMAZIONI \_ SERVER \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**INFORMAZIONI \_ SERVER \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**INFORMAZIONI \_ SERVER \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**INFORMAZIONI \_ SERVER \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**INFORMAZIONI \_ SERVER \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**INFORMAZIONI \_ SERVER \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**INFORMAZIONI \_ SERVER \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**INFORMAZIONI \_ SERVER \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni del server di gestione di rete. Per altre informazioni, vedere [**IADsComputer.**](/windows/desktop/api/iads/nn-iads-iadscomputer)

Per altre informazioni, vedere Funzioni [di trasporto server e workstation.](server-and-workstation-transport-functions.md)

 

 
