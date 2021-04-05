---
title: Accesso alle interfacce tra gli Apartment
description: Accesso alle interfacce tra gli Apartment
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709259"
---
# <a name="accessing-interfaces-across-apartments"></a>Accesso alle interfacce tra gli Apartment

COM consente a qualsiasi Apartment di un processo di ottenere l'accesso a un'interfaccia implementata in un oggetto in qualsiasi altro Apartment nel processo. Questa operazione viene eseguita tramite l'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Questa interfaccia dispone di tre metodi, che consentono di eseguire le operazioni seguenti:

-   Registrare un'interfaccia come interfaccia *globale* (processwide).
-   Ottiene un puntatore a tale interfaccia da qualsiasi altro Apartment tramite un cookie.
-   Revocare la registrazione globale di un'interfaccia.

L'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) rappresenta un modo efficiente per un processo di archiviazione di un puntatore a interfaccia in una posizione di memoria a cui è possibile accedere da più Apartment all'interno del processo, ad esempio variabili a livello di processo e oggetti *agile* (oggetti a thread libero, con marshalling) che contengono puntatori di interfaccia ad altri oggetti.

Un oggetto agile non è a conoscenza dell'infrastruttura COM sottostante in cui viene eseguito. in altre parole, l'Apartment, il contesto e il thread in cui è in esecuzione. È possibile che l'oggetto sia in attesa di interfacce specifiche per un apartment o un contesto. Per questo motivo, la chiamata di queste interfacce da qualsiasi posizione in cui è in esecuzione il componente agile potrebbe non funzionare sempre correttamente. La tabella dell'interfaccia globale evita questo problema garantendo che venga usato un proxy valido (o un puntatore diretto) all'oggetto, in base alla posizione in cui è in esecuzione l'oggetto agile.

> [!Note]  
> La tabella dell'interfaccia globale non è portabile tra i limiti del processo o del computer, quindi non può essere usata al posto del normale meccanismo di passaggio dei parametri.

 

Per informazioni sulla creazione e sull'utilizzo di una tabella di interfaccia globale, vedere gli argomenti seguenti:

-   [Creazione della tabella dell'interfaccia globale](creating-the-global-interface-table.md)
-   [Quando usare la tabella dell'interfaccia globale](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
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

 

 




