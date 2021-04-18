---
title: Modifiche alla route migliore a una rete
description: Una modifica apportata a uno dei valori seguenti per la route migliore a una determinata rete di destinazione determina la generazione di un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298623"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Modifiche alla route migliore a una rete

**Windows Server 2003:** Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le nuove applicazioni devono usare l'API di Routing Table Manager versione 2.

Una modifica apportata a uno dei valori seguenti per la route migliore a una determinata rete di destinazione determina la generazione di un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro:

-   Identificatore di protocollo
-   Indice dell'interfaccia
-   Indirizzo del router hop successivo
-   Dati specifici della famiglia di protocolli che includono metriche di route

Una modifica nell'identificatore del protocollo, nell'indice dell'interfaccia o nell'indirizzo del router di hop successivo si verifica quando viene aggiunta una nuova voce di route migliore o quando la voce di route migliore corrente viene eliminata o obsoleta e lascia un'altra route come nuova route migliore.

 

 




