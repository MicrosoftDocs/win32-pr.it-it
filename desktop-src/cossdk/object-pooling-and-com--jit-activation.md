---
description: L'attivazione JIT COM+ causa essenzialmente una compromissione tra i client greedy e i server greedy per ottenere prestazioni ottimali. I client ottengono i riferimenti agli oggetti, mentre i server possono gestire in modo più accurato l'utilizzo della memoria.
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: Pool di oggetti e attivazione JIT COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401510"
---
# <a name="object-pooling-and-com-jit-activation"></a>Pool di oggetti e attivazione JIT COM+

L'attivazione JIT COM+ causa essenzialmente una compromissione tra i client greedy e i server greedy per ottenere prestazioni ottimali. I client ottengono i riferimenti agli oggetti, mentre i server possono gestire in modo più accurato l'utilizzo della memoria.

È possibile perfezionarlo ulteriormente utilizzando il [pool di oggetti com+](com--object-pooling.md). Raggruppando gli oggetti abilitati per JIT, è possibile dedicare una certa quantità di memoria per conservare un certo numero di oggetti attivi in memoria, pronti per il riutilizzo immediato. Questa operazione è più sensata quando gli oggetti sono costosi da creare, come nel caso in cui contengono più risorse.

In questo modo, è possibile creare un pool di oggetti attivati tramite JIT, in modo da ottenere i vantaggi seguenti:

-   Tempi di riattivazione degli oggetti molto accelerati.
-   Riutilizzo delle risorse costose degli oggetti.
-   Gestione più precisa dell'utilizzo di memoria e risorse per gli oggetti in pool.
-   Conservazione della flessibilità amministrativa in modo che l'applicazione possa essere ridimensionata in modo da usare le risorse disponibili e adattarsi ai requisiti di prestazioni mutevoli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Pool di oggetti COM+](com--object-pooling.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Transazioni e attivazione JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



