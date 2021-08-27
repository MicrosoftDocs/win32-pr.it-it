---
title: Uso di puntatori opachi
description: I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d24524f64fca7062ffb35ed6f4d5e6a2bc935ef7fee0c7fa141cb2e823e70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025071"
---
# <a name="using-opaque-pointers"></a>Uso di puntatori opachi

I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni. Il gestore tabelle di routing consente ai client di archiviare queste informazioni nelle strutture di destinazione nella tabella di routing. Le informazioni vengono archiviate e recuperate usando *puntatori opachi.* Le informazioni archiviate sono private e accessibili solo al client proprietario del puntatore opaco.

Ad esempio, il gestore di gruppi multicast mantiene un elenco di voci di inoltro multicast dipendenti da una destinazione specifica. Il gestore di gruppi multicast usa un puntatore opaco in tale destinazione. In un altro esempio, un protocollo di routing che annuncia una determinata destinazione può mantenere le informazioni correlate al proprio annuncio di route della destinazione usando un puntatore opaco, anche se non è proprietaria della route migliore.

Il numero di puntatori opachi è limitato. questi puntatori vengono allocati ai client in base al primo accesso e al primo servizio. L'amministratore del router deve allocare il numero corretto di puntatori durante la configurazione del router. Pertanto, i protocolli di routing e altri client devono documentare l'uso di puntatori opachi.

 

 




