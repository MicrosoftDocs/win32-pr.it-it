---
title: Informazioni su Multicast Group Manager
description: Questa documentazione descrive la tecnologia MGM (Multicast Group Manager).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Multicast Group Manager RRAS
- Multicast Group Manager RRAS , descritto
- Servizio Routing e Accesso remoto RRAS, Gestione gruppi multicast
- Servizio Routing e Accesso remoto RRAS, Multicast Group Manager, descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f83dc2b212f7d70d04b4a3ec08bf07e664fa2d67d9c638233a4e8e914369c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030931"
---
# <a name="about-multicast-group-manager"></a>Informazioni su Multicast Group Manager

Questa documentazione descrive la tecnologia MGM (Multicast Group Manager).

Il multicast consente a un host di inviare dati solo alle destinazioni che richiedono in modo specifico di ricevere i dati. In questo modo, il multicast differisce dall'invio di dati broadcast, perché i dati trasmessi vengono inviati a tutti gli host.

Il multicast consente di risparmiare larghezza di banda di rete perché i dati multicast vengono ricevuti solo dagli host che richiedono i dati e i dati vengono inviati su qualsiasi collegamento una sola volta. Il multicast consente di risparmiare larghezza di banda del server perché un server deve inviare un solo messaggio multicast per rete anziché un messaggio unicast per ricevitore. Esempi di applicazioni multicast comuni sono riunioni online e radio Internet.

L'API MGM consente agli sviluppatori di scrivere protocolli di routing multicast che interagisce con i router che eseguono il gestore del gruppo multicast.

Quando in un router è abilitato più di un protocollo di routing multicast, il gestore del gruppo multicast coordina le operazioni tra tutti i protocolli di routing. Il gestore del gruppo multicast informa ogni protocollo di routing quando si verificano modifiche all'appartenenza al gruppo e quando vengono ricevuti dati multicast da una nuova origine o destinati a un nuovo gruppo.

L'API MGM offre le funzionalità seguenti:

-   Registrazione del protocollo
-   Gestione di gruppi
-   Enumerazione MFE (Multicast Forwarding Entry)
-   Definizioni di callback per i protocolli di routing multicast

Questa panoramica descrive i componenti dell'architettura multicast, gli scenari client usati per interagire con il gestore di gruppi multicast e considerazioni sulla programmazione per l'uso dell'API MGM.

 

 




