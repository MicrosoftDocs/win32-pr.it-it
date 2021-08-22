---
description: Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si sono verificati determinati eventi di rete.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notifica degli eventi di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794761"
---
# <a name="notification-of-network-events"></a>Notifica degli eventi di rete

Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si sono verificati determinati eventi di rete. L'elenco degli eventi di rete definiti è costituito dai seguenti elementi:

-   **FD \_ CONNECT:** è stata completata una connessione a un host remoto o a una sessione multicast.
-   **FD \_ ACCEPT:** un host remoto sta effettuando una richiesta di connessione.
-   **FD \_ READ:** sono arrivati i dati di rete disponibili per la lettura.
-   **FD \_ WRITE:** lo spazio è diventato disponibile nei buffer del provider di servizi in modo che ora sia possibile inviare dati aggiuntivi.
-   **FD \_ OOB:** i dati fuori banda sono disponibili per la lettura.
-   **FD \_ CLOSE:** l'host remoto ha chiuso la connessione.
-   **FD \_ QOS:** si è verificata una modifica nei livelli QoS negoziati.
-   **FD \_ GROUP \_ QOS**: riservato.
-   **FD \_ ROUTING \_ INTERFACE \_ CHANGE:** un'interfaccia locale che deve essere usata per raggiungere la destinazione specificata in **SIO ROUTING INTERFACE CHANGE \_ \_ \_ IOCTL** è stata modificata.
-   **FD \_ ADDRESS \_ LIST \_ CHANGE**: l'elenco di indirizzi locali a cui l'applicazione può eseguire l'associazione è stato modificato.

Il set di eventi di rete enumerati in precedenza viene talvolta definito **eventi FD \_ XXX.** L'indicazione dell'occorrenza di uno o più di tali eventi di rete può essere specificata in diversi modi, a seconda del modo in cui il client richiede la notifica.

 

 



