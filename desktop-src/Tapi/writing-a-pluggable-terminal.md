---
description: In genere, un provider di servizi multimediali implementa la creazione del terminale.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Scrittura di un terminale collegabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526809"
---
# <a name="writing-a-pluggable-terminal"></a>Scrittura di un terminale collegabile

In genere, un provider di servizi multimediali implementa la creazione del terminale. A partire da Windows 2000 SP1, TAPI 3 include terminali innestabili che consentono a un'applicazione di implementare la creazione del terminale. Per altre informazioni sull'uso di questi terminali, vedere Panoramica sull' [implementazione di terminali collegabili](implementing-pluggable-terminals.md) .

Non usare i terminali collegabili regolarmente perché le funzionalità complete di un terminale saranno disponibili solo quando un MSP ne è pienamente a conoscenza. Inoltre, è consigliabile non tentare di implementare terminali innestabili, a meno che non si abbia già familiarità con la scrittura di provider di servizi multimediali. Le tecniche e i potenziali problemi interessati sono molto simili.

Il provisioning di un caso speciale di terminale collegabile è attualmente disponibile per la situazione di un server di conferenza che deve aggiungere client non Windows 2000 SP1 o non multicast H. 323 a conferenze multicast SDP/IP a più parti di TAPI 3.

 

 



