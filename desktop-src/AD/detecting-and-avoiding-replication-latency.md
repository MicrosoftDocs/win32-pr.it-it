---
title: Rilevamento ed evitare la latenza di replica
description: La latenza di replica è un fatto di vita in un sistema distribuito ad accoppiato libero.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27540a5756d2059cc96db8941a939637aaa45b387cf2d451c56c3e8b43d1b966
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019436"
---
# <a name="detecting-and-avoiding-replication-latency"></a>Rilevamento ed evitare la latenza di replica

La latenza di replica è un fatto di vita in un sistema distribuito ad accoppiato libero. Le applicazioni devono soddisfare questo problema. Il modo migliore per gestire la latenza di replica è progettare applicazioni per ridurre al minimo gli effetti. L'applicazione ideale abilitata per la directory:

-   Non fa distinzione tra l'avaria della versione.
-   Non dipende dalle relazioni tra più oggetti.
-   Non ha requisiti di coerenza intra-oggetto o inter-oggetto.

Le applicazioni e i servizi che si adattano a questo profilo non devono preoccuparsi della latenza di replica. Altre applicazioni devono essere progettate in base alla latenza di replica. La chiave per il successo della progettazione di un'applicazione di questo tipo è la consapevolezza del processo di replica. I passaggi eseguiti in fase di progettazione per ridurre le dipendenze tra oggetti e ridurre al minimo le finestre di aggiornamento parziale pagheranno grandi dividendi in fase di esecuzione. Gli approcci alla gestione della latenza di replica sono suddivisi in due classi: strategie di prevenzione che riducono l'impatto delle strategie di latenza e rilevamento che consentono a un'applicazione di rilevare gli stati indotta dalla latenza.

 

 




