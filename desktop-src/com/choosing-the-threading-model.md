---
title: Scelta del modello di threading
description: Scelta del modello di threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396782"
---
# <a name="choosing-the-threading-model"></a>Scelta del modello di threading

La scelta del modello di threading per un oggetto dipende dalla funzione dell'oggetto. Un oggetto che esegue l'I/O esteso può supportare il threading libero per fornire la massima risposta ai client consentendo chiamate di interfaccia durante la latenza di I/O. D'altra parte, un oggetto che interagisce con l'utente potrebbe supportare il threading di Apartment per sincronizzare le chiamate COM in ingresso con le relative operazioni della finestra.

È più facile supportare il threading di Apartment negli appartamenti a thread singolo poiché COM fornisce la sincronizzazione in base alle singole chiamate. Il supporto del threading libero è più difficile perché l'oggetto deve implementare la sincronizzazione. Tuttavia, la risposta ai client potrebbe essere migliore perché la sincronizzazione può essere implementata per sezioni più piccole di codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Apartment con multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 




