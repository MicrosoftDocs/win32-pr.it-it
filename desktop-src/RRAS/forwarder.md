---
title: Server d'inoltro
description: Il server d'trasmissione è il componente in modalità kernel del router responsabile dell'invio dei dati da un'interfaccia del router alle altre.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044762"
---
# <a name="forwarder"></a>Server d'inoltro

Il server d'trasmissione è il componente in modalità kernel del router responsabile dell'invio dei dati da un'interfaccia del router alle altre. Il server d'inoltre decide inoltre se un pacchetto è destinato al recapito locale, se è destinato all'uscita da un'altra interfaccia o a entrambi.

Sono disponibili due server d'avvio in modalità kernel: unicast e multicast.

Gestione router ottiene le route migliori per tutte le destinazioni da Gestione tabelle di routing. Queste route vengono passate al server d'avvio unicast. Il server d'avvio unicast usa queste route per eseguire l'effettivo invio di dati unicast. In questo modo, il server d'inoltro unicast gestisce una cache delle route migliori nella visualizzazione unicast della tabella di routing.

Il gestore del gruppo multicast utilizza le informazioni della visualizzazione multicast della tabella di routing per aggiungere le voci di inoltro multicast al server di inoltro multicast.

 

 




