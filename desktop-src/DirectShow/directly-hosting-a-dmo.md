---
description: Hosting diretto di un DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hosting diretto di un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747658"
---
# <a name="directly-hosting-a-dmo"></a>Hosting diretto di un DMO

Questa sezione descrive il modo in cui un'applicazione può fungere da client diretto di un DMO. L'applicazione recapita input a DMO, DMO crea l'output e l'applicazione usa l'output per il rendering, l'ulteriore elaborazione o qualsiasi altro elemento. L'applicazione è responsabile di problemi quali allocazione della memoria, temporizzazione e sincronizzazione e Threading. Questi requisiti variano in base alla natura dell'applicazione.

Le informazioni contenute in questa sezione si applicano anche se si sta scrivendo un componente che funge da livello tra un'applicazione e un DMO (ad esempio, un controllo ActiveX che ospita un DMO). Inoltre, è consigliabile leggere questa sezione se si sta scrivendo un DMO, perché descrive le funzionalità che devono essere implementate da DMO.

Questa sezione contiene i seguenti argomenti:

-   [Impostazione dei tipi di supporto in un DMO](setting-media-types-on-a-dmo.md)
-   [Elaborazione di dati in un DMO](processing-data-in-a-dmo.md)
-   [Elaborazione sul posto](in-place-processing.md)
-   [Flussi facoltativi](optional-streams.md)
-   [Implementazione di IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DMOs](using-dmos.md)
</dt> </dl>

 

 



