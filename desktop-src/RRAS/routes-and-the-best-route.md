---
title: Route e migliore route
description: Una route è un \ 0034; percorso di rete \ 0034; a una destinazione a cui è associato un determinato costo. Il costo è rappresentato dalle relative preferenze amministrative e dalla metrica specifica del protocollo. Le route con costi inferiori sono preferite rispetto a tutte le altre route.
ms.assetid: c5a75308-42da-4ef9-a712-9987c87eef84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd55ec1188383f4cdef55511aae7a9c2cf59303
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298990"
---
# <a name="routes-and-the-best-route"></a>Route e migliore route

Una route è un "percorso di rete" per una destinazione a cui è associato un determinato costo. Il costo è rappresentato dalle relative preferenze amministrative e dalla metrica specifica del protocollo. Le route con costi inferiori sono preferite rispetto a tutte le altre route.

Una voce di route nella tabella di routing include:

-   Handle per la destinazione
-   Proprietario della route
-   Neighbor (peer) che ha fornito le informazioni sulla Route
-   Flag associati allo stato della route
-   Flag associati alla route
-   Preferenza e metrica per la route
-   Elenco di visualizzazioni a cui appartiene la route
-   Informazioni private del proprietario della route
-   Elenco di hop successivi utilizzati per raggiungere la destinazione

I valori seguenti, insieme, identificano in modo univoco una route nella tabella di routing:

-   Rete di destinazione
-   Proprietario della route
-   Il vicino che ha fornito la route

## <a name="metrics-and-preference"></a>Metriche e preferenze

Ogni route ha una preferenza amministrativa (specificata dai criteri di routing) e una metrica dipendente dal client. Gestione tabelle di routing utilizza queste informazioni per determinare quale route è la migliore route a una destinazione. Le route con preferenza inferiore sono Route migliori, una più bassa e quindi migliore. Se due route hanno la stessa preferenza, la route con la metrica inferiore rappresenta il percorso migliore.

In genere, la preferenza di una route è determinata dalla preferenza del client che ha aggiunto la route. Tuttavia, per tutte le route aggiunte mediante lo strumento di gestione Netsh.exe, è possibile specificare un valore di preferenza per ogni route.

La preferenza viene in genere utilizzata per indicare la priorità tra i client. Ad esempio, un amministratore può assegnare a OSPF una preferenza più bassa (migliore) rispetto a RIP. In questo caso, le route OSPF sono preferibili per la copia delle route.

 

 




