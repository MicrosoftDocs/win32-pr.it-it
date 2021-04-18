---
title: Informazioni su Gestione gruppi multicast
description: Questa documentazione descrive la tecnologia di gestione dei gruppi multicast (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gestione gruppo multicast RRAS
- Gestore del gruppo multicast RRAS, descritto
- Servizio Routing e accesso remoto RRAS, gestione gruppo multicast
- Servizio Routing e accesso remoto RRAS, gestione gruppo multicast, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298294"
---
# <a name="about-multicast-group-manager"></a>Informazioni su Gestione gruppi multicast

Questa documentazione descrive la tecnologia di gestione dei gruppi multicast (MGM).

Il multicast consente a un host di inviare dati solo alle destinazioni che richiedono la ricezione dei dati in modo specifico. In questo modo, il multicasting è diverso dall'invio di dati broadcast, dal momento che i dati di trasmissione vengono inviati a tutti gli host.

Il multicast consente di risparmiare larghezza di banda poiché i dati multicast vengono ricevuti solo da tali host che richiedono i dati e i dati vengono trasmessi su qualsiasi collegamento una sola volta. Il multicast consente di risparmiare larghezza di banda del server poiché un server deve inviare un solo messaggio multicast per rete anziché un messaggio unicast per ricevitore. Esempi di applicazioni multicast più diffuse sono incontri online e Internet radio.

L'API MGM consente agli sviluppatori di scrivere protocolli di routing multicast che interagiscono con i router che eseguono il gestore del gruppo multicast.

Quando in un router è abilitato più di un protocollo di routing multicast, il gestore del gruppo multicast coordina le operazioni tra tutti i protocolli di routing. Il gestore del gruppo multicast informa ogni protocollo di routing quando si verificano modifiche all'appartenenza al gruppo e quando vengono ricevuti i dati multicast da una nuova origine o destinata a un nuovo gruppo.

L'API MGM offre le funzionalità seguenti:

-   Registrazione del protocollo
-   Gestione di gruppi
-   Enumerazione MFE (multicast inoltring entry)
-   Definizioni di callback per i protocolli di routing multicast

Questa panoramica descrive i componenti dell'architettura multicast, gli scenari client usati per interagire con gestione gruppi multicast e le considerazioni sulla programmazione per l'uso dell'API MGM.

 

 




