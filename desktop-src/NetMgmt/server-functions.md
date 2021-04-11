---
title: Funzioni server (gestione della rete)
description: Le funzioni del server di gestione di rete eseguono attività amministrative su un server locale o remoto. Le funzioni server sono elencate di seguito.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047764"
---
# <a name="server-functions-network-management"></a>Funzioni server (gestione della rete)

Le funzioni del server di gestione di rete eseguono attività amministrative su un server locale o remoto. Le funzioni server sono elencate di seguito.



| Funzione                                       | Descrizione                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Restituisce un elenco di unità disco locali in un server.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Elenca tutti i server visibili di un tipo o di tipi specifici nel dominio specificato. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Restituisce le informazioni di configurazione relative a un server specificato.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Imposta i parametri operativi per un server.                                        |



 

Solo un utente o un'applicazione con appartenenza a un gruppo amministratore in un server locale o remoto può eseguire attività amministrative su tale server per controllare l'operazione del server, l'accesso degli utenti e la condivisione delle risorse. I parametri di basso livello che interessano l'operazione di un server possono essere esaminati e modificati chiamando le funzioni [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) . Questi parametri vengono definiti nel file di LANMAN.INI del server.

La maggior parte delle funzioni del server di gestione di rete viene eseguita solo su un server remoto. La funzione [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) viene eseguita su una workstation locale o su un server remoto. Se si tenta di eseguire altre funzioni server su una workstation locale, le funzioni restituiscono l'errore NERR \_ RemoteOnly.

Le informazioni specifiche del server sono disponibili ai livelli seguenti:

-   [**\_Informazioni SERVER \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**\_Informazioni SERVER \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**\_Informazioni SERVER \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**\_Informazioni SERVER \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**\_Informazioni SERVER \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**\_Informazioni SERVER \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**\_Informazioni SERVER \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**\_Informazioni SERVER \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**\_Informazioni SERVER \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**\_Informazioni SERVER \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**\_Informazioni SERVER \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**\_Informazioni SERVER \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**\_Informazioni SERVER \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**\_Informazioni SERVER \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**\_Informazioni SERVER \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**\_Informazioni SERVER \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**\_Informazioni SERVER \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**\_Informazioni SERVER \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**\_Informazioni SERVER \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**\_Informazioni SERVER \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**\_Informazioni SERVER \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**\_Informazioni SERVER \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**\_Informazioni SERVER \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**\_Informazioni SERVER \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**\_Informazioni SERVER \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**\_Informazioni SERVER \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**\_Informazioni SERVER \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**\_Informazioni SERVER \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**\_Informazioni SERVER \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**\_Informazioni SERVER \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**\_Informazioni SERVER \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni del server di gestione di rete. Per ulteriori informazioni, vedere [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Per ulteriori informazioni, vedere le [funzioni di trasporto server e workstation](server-and-workstation-transport-functions.md).

 

 
