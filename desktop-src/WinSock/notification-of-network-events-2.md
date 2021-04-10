---
description: Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si verificano determinati eventi di rete.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notifica degli eventi di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879193"
---
# <a name="notification-of-network-events"></a>Notifica degli eventi di rete

Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si verificano determinati eventi di rete. L'elenco degli eventi di rete definiti è costituito dagli elementi seguenti:

-   **FD \_ Connetti**: è stata completata una connessione a un host remoto o a una sessione multicast.
-   **FD \_ ACCEPT**: un host remoto sta effettuando una richiesta di connessione.
-   **FD \_ READ**: sono arrivati i dati di rete che è possibile leggere.
-   **FD \_ WRITE**: lo spazio è diventato disponibile nei buffer del provider di servizi, in modo che ora possano essere inviati dati aggiuntivi.
-   **FD \_ OOB**: i dati fuori banda sono disponibili per la lettura.
-   **FD \_ CLOSE**: l'host remoto ha chiuso la connessione.
-   **FD \_ QOS**: si è verificata una modifica nei livelli QoS negoziato.
-   **FD \_ \_QoS del gruppo**: riservato.
-   **FD \_ \_ \_ Modifica dell'interfaccia di routing**: un'interfaccia locale da usare per raggiungere la destinazione specificata nell' **interfaccia di \_ routing sio \_ \_ modificare IOCTL** è cambiata.
-   **FD \_ \_ \_ Modifica elenco indirizzi**: l'elenco degli indirizzi locali a cui è possibile associare l'applicazione è stato modificato.

Il set di eventi di rete enumerato in precedenza viene talvolta indicato come evento **FD \_ xxx** . L'indicazione dell'occorrenza di uno o più eventi di rete di questo tipo può essere fornita in diversi modi, a seconda del modo in cui il client richiede la notifica.

 

 



