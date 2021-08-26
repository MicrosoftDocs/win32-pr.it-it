---
description: Hosting diretto di un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hosting diretto di un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f421ed470ae1d39c04054e1cb4ec6252652ed2083ea336a58525f60a6e525b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982991"
---
# <a name="directly-hosting-a-dmo"></a>Hosting diretto di un DMO

Questa sezione descrive come un'applicazione può fungere da client diretto di un DMO. L'applicazione fornisce input al DMO, il DMO crea l'output e l'applicazione usa l'output per il rendering, l'ulteriore elaborazione o qualsiasi altro elemento. L'applicazione è responsabile di problemi quali l'allocazione della memoria, la tempistica e la sincronizzazione e il threading. Questi requisiti dipendono dalla natura dell'applicazione.

Le informazioni contenute in questa sezione si applicano anche se si scrive un componente che funge da livello tra un'applicazione e un DMO (ad esempio, un controllo ActiveX che ospita un DMO). È anche consigliabile leggere questa sezione se si scrive un DMO, perché descrive le funzionalità che l'DMO deve implementare.

Questa sezione contiene i seguenti argomenti:

-   [Impostazione dei tipi di supporti in un DMO](setting-media-types-on-a-dmo.md)
-   [Elaborazione di dati in un DMO](processing-data-in-a-dmo.md)
-   [Elaborazione sul posto](in-place-processing.md)
-   [Facoltativo Flussi](optional-streams.md)
-   [Implementazione di IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DMO](using-dmos.md)
</dt> </dl>

 

 



