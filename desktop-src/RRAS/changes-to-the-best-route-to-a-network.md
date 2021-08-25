---
title: Modifiche alla route migliore per una rete
description: Una modifica in uno dei valori seguenti per la route migliore a una determinata rete di destinazione fa sì che il gestore tabelle di routing generi un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fe96a0b339325c2290c346ba581d5b892db24d1cd972f7a83a0b2ec525eeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030361"
---
# <a name="changes-to-the-best-route-to-a-network"></a>Modifiche alla route migliore per una rete

**Windows Server 2003:** Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le nuove applicazioni devono usare l'API Gestione tabelle di routing versione 2.

Una modifica in uno dei valori seguenti per la route migliore a una determinata rete di destinazione fa sì che il gestore tabelle di routing generi un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro:

-   Identificatore di protocollo
-   Indice dell'interfaccia
-   Indirizzo del router dell'hop successivo
-   Dati specifici della famiglia di protocolli che includono metriche di route

Una modifica nell'identificatore di protocollo, nell'indice dell'interfaccia o nell'indirizzo del router dell'hop successivo si verifica quando viene aggiunta una nuova voce di route migliore o quando la voce di route migliore corrente viene eliminata o obsoleta e lascia un'altra route come nuova route migliore.

 

 




