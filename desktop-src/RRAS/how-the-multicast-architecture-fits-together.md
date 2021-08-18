---
title: Come si inserisce l'architettura multicast
description: Questa sezione descrive una configurazione di esempio e il modo in cui i componenti principali si uniscono.
ms.assetid: 1fa0b343-0276-402b-8c3d-5ca114ad43cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94f4ca79b9fdd6b2e2fd9e75dc61d780af4380ed958a491f69231f7d541f0aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791330"
---
# <a name="how-the-multicast-architecture-fits-together"></a>Come si inserisce l'architettura multicast

Questa sezione descrive una configurazione di esempio e il modo in cui i componenti principali si uniscono.

Nella figura seguente viene illustrata la relazione tra i vari componenti di un router.

![relazione tra i componenti del router Windows 2000](images/mrarch1.png)

Il gestore del gruppo multicast fa parte del servizio RRAS in esecuzione in un server che opera come router.

Sul router visualizzato sono in esecuzione tre protocolli di routing multicast (Protocollo 1, Protocollo 2, Protocollo 3). Ogni protocollo può essere proprietario di una o più interfacce (in questa illustrazione, il protocollo 1 è proprietario dell'interfaccia 1, il protocollo 2 è proprietario dell'interfaccia 2 e il protocollo 3 è proprietario dell'interfaccia 3). Ogni interfaccia può essere di proprietà di un solo protocollo di routing (oltre a IGMP, che è un caso speciale).

Il gestore di gruppi multicast viene eseguito sul router e coordina la distribuzione delle informazioni sui gruppi tra i protocolli di routing.

Nella figura seguente viene illustrata la relazione tra due router in un'architettura multicast.

![relazione tra due router nell'architettura multicast](images/mrarch2.png)

Nella figura precedente, il Router 2 invia un messaggio multicast alla rete 2 sull'interfaccia 3. Il router 1 riceve il messaggio multicast dalla rete 2 sull'interfaccia 3. Su entrambi i router, il protocollo 3 è proprietario dell'interfaccia 3 corrispondente.

La figura seguente mostra il percorso di un messaggio da un'origine multicast (a un gruppo multicast) per raggiungere l'host aggiunto al gruppo multicast. I router nella figura usano la stessa configurazione delle illustrazioni precedenti. Tuttavia, i dettagli dell'interfaccia e del protocollo non vengono visualizzati per mantenere semplice la figura.

![percorso del messaggio dall'origine multicast all'host di destinazione](images/mrarch3.png)

Lo scenario seguente descrive gli eventi che si verificano quando un host si aggiunge a un gruppo multicast. Fare riferimento alla figura precedente per le relazioni tra le varie entità.

1.  Host 1 aggiunge il gruppo multicast G sulla rete 3.
2.  Il router 3 apprende G tramite IGMP.
3.  Il gestore del gruppo multicast sul Router 3 notifica al protocollo 3 sul router 3 che sono presenti nuovi ricevitori per G.
4.  Il protocollo 3 sul router 3 invia quindi una notifica al protocollo 3 sul router 1 su G.
5.  A sua volta, il protocollo 3 sul router 1 invia una notifica al gestore del gruppo multicast sul Router 1 su G.
6.  Il gestore del gruppo multicast sul Router 1 invia quindi una notifica al protocollo 1 e al protocollo 2 su G.
7.  Il protocollo 2 può informare il router 2 su G, se il protocollo è progettato a tale scopo.

Nello scenario seguente vengono descritti gli eventi che si verificano quando un messaggio viene inviato a un gruppo multicast. Fare riferimento alla figura precedente per le relazioni tra le diverse entità.

1.  Un'origine nella rete 1 invia un messaggio al gruppo G.
2.  Il messaggio inviato dall'origine S passa prima al Router 2, che quindi lo inoltra al Router 1 usando l'interfaccia 2 (poiché il router 2 è stato informato dal protocollo 2 che i ricevitori sono presenti a valle).
3.  Il router 1 inoltra il messaggio al Router 3(poiché il router 1 è stato informato dal protocollo 2 che i ricevitori sono presenti a valle).
4.  Il router 3 inoltra il messaggio alla rete 3 e pertanto arriva all'host 1.

Per altre informazioni sull'interazione del protocollo di routing multicast, vedere [RFC 2715](routing-protocols-request-for-comments.md), Regole di interoperabilità per i protocolli di routing multicast.

 

 




