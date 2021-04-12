---
title: Comunicazione Single-Threaded e multithreading
description: Comunicazione Single-Threaded e multithreading
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329303"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Comunicazione Single-Threaded e multithreading

Un client o un server che supporta gli Apartment a thread singolo e a thread multipli avrà un apartment multithread, che contiene tutti i thread inizializzati come a thread libero e uno o più Apartment a thread singolo. È necessario effettuare il marshalling di puntatori di interfaccia tra Apartment, ma è possibile usare senza marshalling in un Apartment. Le chiamate agli oggetti in un Apartment a thread singolo verranno sincronizzate da COM. Le chiamate a oggetti nell'Apartment con multithreading non verranno sincronizzate da COM.

Tutte le informazioni sugli Apartment a thread singolo si applicano ai thread contrassegnati come modello di Apartment e tutte le informazioni sugli Apartment con multithreading si applicano a tutti i thread contrassegnati come a thread libero. Le regole di threading dell'Apartment si applicano alla comunicazione tra Apartment, che richiede il marshalling dei puntatori di interfaccia tra gli appartamenti con chiamate a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) e [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), come descritto in [Apartment a thread singolo](single-threaded-apartments.md).

> [!Note]  
> Quando si gestiscono server in-process, è necessario tenere presenti alcune considerazioni speciali. Per ulteriori informazioni, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartment con multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 




