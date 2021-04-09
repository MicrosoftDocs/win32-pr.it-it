---
title: Utilizzo di puntatori opachi
description: I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856533"
---
# <a name="using-opaque-pointers"></a>Utilizzo di puntatori opachi

I client spesso devono archiviare informazioni aggiuntive specifiche del client sulle destinazioni. Gestione tabelle di routing consente ai client di archiviare queste informazioni in strutture di destinazione nella tabella di routing. Le informazioni vengono archiviate e recuperate tramite *puntatori opachi*. Le informazioni archiviate sono private e accessibili solo al client proprietario del puntatore opaco.

Il gestore del gruppo multicast, ad esempio, mantiene un elenco di voci di invio multicast che dipendono da una determinata destinazione. Il gestore del gruppo multicast utilizza un puntatore opaco in tale destinazione. In un altro esempio, un protocollo di routing che annuncia una determinata destinazione può contenere informazioni correlate alla propria inserzione di route della destinazione utilizzando un puntatore opaco, anche se non è il proprietario della route migliore.

Il numero di puntatori opachi è limitato; questi puntatori vengono allocati ai client in base a una prima, prima di tutto. L'amministratore del router deve allocare il numero corretto di puntatori durante la configurazione del router; Pertanto, i protocolli di routing e gli altri client devono documentare l'utilizzo di puntatori opachi.

 

 




