---
title: Rilevamento ed evitare la latenza di replica
description: La latenza di replica è un fatto di vita in un sistema distribuito a regime di controllo libero.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707720"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Rilevamento ed evitare la latenza di replica

La latenza di replica è un fatto di vita in un sistema distribuito a regime di controllo libero. Le applicazioni devono soddisfare questa esigenza. Il modo migliore per gestire la latenza di replica consiste nel progettare le applicazioni per ridurre al minimo gli effetti. Applicazione ideale abilitata per la directory:

-   Non è sensibile all'inclinazione della versione.
-   Non dipende dalle relazioni tra più oggetti.
-   Non presenta requisiti di coerenza intra-o tra oggetti.

Le applicazioni e i servizi che soddisfano questo profilo non devono preoccuparsi della latenza di replica. Le altre applicazioni devono essere progettate tenendo presente la latenza di replica. La chiave per il successo nella progettazione di un'applicazione di questo tipo è la consapevolezza del processo di replica. I passaggi eseguiti in fase di progettazione per ridurre le dipendenze tra oggetti e ridurre al minimo le finestre degli aggiornamenti parziali pagheranno dividendi di grandi dimensioni in fase di esecuzione. Gli approcci alla gestione della latenza di replica sono divisi in due classi, ovvero strategie di prevenzione che riducono l'effetto delle strategie di latenza e rilevamento che consentono a un'applicazione di rilevare gli stati indotti dalla latenza.

 

 




