---
title: Single-Threaded e multithreading
description: Single-Threaded e multithreading
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1096ff2cd5916bf16b00a746c2e6de6ce22008258c6e200c2858c0430cb3f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129833"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded e multithreading

Un client o un server che supporta apartment a thread singolo e multithreading avrà un apartment a thread multipli, contenente tutti i thread inizializzati come apartment a thread libero e uno o più apartment a thread singolo. I puntatori a interfaccia devono essere sottoposti a marshalling tra apartment, ma possono essere usati senza effettuare il marshalling all'interno di un apartment. Le chiamate agli oggetti in un apartment a thread singolo verranno sincronizzate da COM. Le chiamate agli oggetti nell'apartment multithreading non verranno sincronizzate da COM.

Tutte le informazioni sugli apartment a thread singolo si applicano ai thread contrassegnati come modello apartment e tutte le informazioni sugli apartment a thread multipli si applicano a tutti i thread contrassegnati come a thread libero. Le regole di threading apartment si applicano alla comunicazione tra apartment, richiedendo il marshalling dei puntatori a interfaccia tra apartment con chiamate a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) e [**CoGetInterfaceAndReleaseStream,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)come descritto in Apartment a thread [singolo.](single-threaded-apartments.md)

> [!Note]  
> Quando si gestiscono server in-process, è necessario tenere presenti alcune considerazioni speciali. Per altre informazioni, vedere [Problemi di threading del server in-process.](in-process-server-threading-issues.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartment multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Apartment a thread singolo](single-threaded-apartments.md)
</dt> </dl>

 

 




