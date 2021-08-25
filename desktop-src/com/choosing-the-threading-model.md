---
title: Scelta del modello di threading
description: Scelta del modello di threading
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1966a4b000683bb7549ce9c825051324088fd85c41146137443045785b5e0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896511"
---
# <a name="choosing-the-threading-model"></a>Scelta del modello di threading

La scelta del modello di threading per un oggetto dipende dalla funzione dell'oggetto. Un oggetto che esegue operazioni di I/O estese potrebbe supportare il free threading per fornire la massima risposta ai client consentendo chiamate di interfaccia durante la latenza di I/O. D'altra parte, un oggetto che interagisce con l'utente potrebbe supportare il threading apartment per sincronizzare le chiamate COM in ingresso con le operazioni della finestra.

È più semplice supportare il threading apartment in apartment a thread singolo perché COM fornisce la sincronizzazione in base alle chiamate. Il supporto del free threading è più difficile perché l'oggetto deve implementare la sincronizzazione. Tuttavia, la risposta ai client può essere migliore perché la sincronizzazione può essere implementata per sezioni di codice più piccole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Apartment multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 




