---
title: Interazione tra l'architettura multicast
description: In questa sezione viene descritta una configurazione di esempio e il modo in cui i componenti principali si adattano insieme.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc82178568bac01e89eb0a4d6ea9222d45e7f5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221674"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Interazione tra l'architettura multicast

In questa sezione viene descritta una configurazione di esempio e il modo in cui i componenti principali si adattano insieme.

Nella figura seguente viene illustrata la relazione tra i vari componenti di un router.

![relazione tra i componenti del router Windows 2000](images/mrarch1.png)

Il gestore del gruppo multicast fa parte del servizio RRAS eseguito in un server che funziona come router.

Il router visualizzato presenta tre protocolli di routing multicast (protocollo 1, protocollo 2, protocollo 3) in esecuzione su di esso. Ogni protocollo può essere proprietario di una o più interfacce (in questa illustrazione, il protocollo 1 è proprietario dell'interfaccia 1, il protocollo 2 possiede l'interfaccia 2 e il protocollo 3 è proprietario dell'interfaccia 3). Ogni interfaccia può essere di proprietà di un solo protocollo di routing (oltre a IGMP, che è un caso speciale).

Il gestore del gruppo multicast viene eseguito sul router e coordina la distribuzione delle informazioni sul gruppo tra i protocolli di routing.

Nella figura seguente viene illustrata la relazione tra due router in un'architettura multicast.

![relazione tra due router nell'architettura multicast](images/mrarch2.png)

Nella figura precedente, il router 2 Invia un messaggio multicast alla rete 2 sull'interfaccia 3. Il router 1 riceve il messaggio multicast dalla rete 2 sull'interfaccia 3. In entrambi i router il protocollo 3 è proprietario della rispettiva interfaccia 3.

Nella figura seguente viene illustrato il percorso di un messaggio da un'origine multicast (a un gruppo multicast) per raggiungere l'host che è stato aggiunto al gruppo multicast. I router nell'illustrazione usano la stessa configurazione delle illustrazioni precedenti. Tuttavia, i dettagli dell'interfaccia e del protocollo non vengono visualizzati per semplificare la figura.

![percorso del messaggio dall'origine multicast all'host di destinazione](images/mrarch3.png)

Nello scenario seguente vengono descritti gli eventi che si verificano quando un host viene aggiunto a un gruppo multicast. Vedere la figura precedente per le relazioni tra le diverse entità.

1.  L'host 1 partecipa al gruppo multicast G sulla rete 3.
2.  Il router 3 apprende informazioni su G tramite IGMP.
3.  Il gestore del gruppo multicast sul router 3 informa il protocollo 3 sul router 3 che sono presenti nuovi ricevitori per G.
4.  Il protocollo 3 sul router 3 notifica quindi il protocollo 3 sul router 1 circa G.
5.  Il protocollo 3 sul router 1 informa a sua volta il gestore del gruppo multicast sul router 1 circa G.
6.  Il gestore del gruppo multicast sul router 1 informa quindi il protocollo 1 e il protocollo 2 circa G.
7.  Il protocollo 2 potrebbe informare il router 2 circa G, se il protocollo è stato progettato per farlo.

Nello scenario seguente vengono descritti gli eventi che si verificano quando un messaggio viene inviato a un gruppo multicast. Fare riferimento alla figura precedente per le relazioni tra le diverse entità.

1.  Un'origine sulla rete 1 Invia un messaggio al gruppo G.
2.  Il messaggio inviato dall'origine S passa prima al router 2, che lo inoltra al router 1 usando l'interfaccia 2 (poiché il router 2 è stato informato dal protocollo 2 che i destinatari sono presenti a valle).
3.  Il router 1 trasmette il messaggio al router 3 (poiché il router 1 è stato informato dal protocollo 2 che i destinatari sono presenti a valle).
4.  Il router 3 Invia il messaggio alla rete 3 e pertanto arriva all'host 1.

Per ulteriori informazioni sull'interazione del protocollo di routing multicast, vedere [RFC 2715](routing-protocols-request-for-comments.md), regole di interoperabilità per i protocolli di routing multicast.

 

 




