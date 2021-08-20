---
title: Accesso alle interfacce tra apartment
description: Accesso alle interfacce tra apartment
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89e82fa29e768328e6c110349627d32e92ab010ce61fdf64141ad3ca7fe9a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048919"
---
# <a name="accessing-interfaces-across-apartments"></a>Accesso alle interfacce tra apartment

COM consente a qualsiasi apartment in un processo di ottenere l'accesso a un'interfaccia implementata in un oggetto in qualsiasi altro apartment del processo. Questa operazione viene eseguita tramite [**l'interfaccia IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Questa interfaccia dispone di tre metodi, che consentono di eseguire le operazioni seguenti:

-   Registrare un'interfaccia *come interfaccia* globale (a livello di processo).
-   Ottenere un puntatore a tale interfaccia da qualsiasi altro apartment tramite un cookie.
-   Revocare la registrazione globale di un'interfaccia.

L'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) è un modo efficiente per un processo di archiviare un puntatore a interfaccia in una posizione di memoria accessibile da più apartment all'interno del processo, ad esempio variabili a livello di processo e oggetti *Agile* (oggetti con thread libero e con marshalling) contenenti puntatori di interfaccia ad altri oggetti.

Un oggetto Agile non è a conoscenza dell'infrastruttura COM sottostante in cui viene eseguito. in altre parole, su quale apartment, contesto e thread è in esecuzione. L'oggetto può essere in attesa di interfacce specifiche di un apartment o di un contesto. Per questo motivo, la chiamata di queste interfacce da qualsiasi posizione di esecuzione del componente Agile potrebbe non funzionare sempre correttamente. La tabella di interfaccia globale evita questo problema assicurando l'uso di un proxy valido (o puntatore diretto) all'oggetto, in base alla posizione in cui è in esecuzione l'oggetto Agile.

> [!Note]  
> La tabella di interfaccia globale non è portabile oltre i limiti del processo o del computer, quindi non può essere usata al posto del normale meccanismo di passaggio dei parametri.

 

Per informazioni sulla creazione e sull'uso di una tabella di interfaccia globale, vedere gli argomenti seguenti:

-   [Creazione della tabella di interfaccia globale](creating-the-global-interface-table.md)
-   [Quando usare la tabella di interfaccia globale](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
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

 

 




