---
description: Concetti relativi alle partizioni COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Concetti relativi alle partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c4a2aaaf44d7c4346e4de44cfdb59ca0d75e593122342afe875a6eea71d9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307968"
---
# <a name="com-partitions-concepts"></a>Concetti relativi alle partizioni COM+

Negli ambienti di elaborazione in cui è necessario usare versioni o configurazioni diverse di un'applicazione nello stesso computer, possono verificarsi conflitti quando una versione dell'applicazione richiede componenti diversi rispetto all'altra o quando una versione richiede un componente nel computer che non è compatibile con l'altra versione dell'applicazione. In passato, l'unico modo per risolvere questo problema era mantenere più computer ed eseguire una versione diversa dell'applicazione in ogni computer. Questo approccio è dis costoso e inefficiente perché aumenta i costi hardware e il sovraccarico amministrativo.

COM+ risolve questo problema fornendo la funzionalità partizioni COM+. È possibile usare partizioni COM+ per installare versioni diverse di un'applicazione COM+ in un computer ed eseguirle contemporaneamente.

Per comprendere e usare questa funzionalità, vedere gli argomenti seguenti:

-   [Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
-   [Implementazione della partizione](partition-implementation.md)
-   [Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
-   [Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
-   [Restrizioni di progettazione delle applicazioni](application-design-restrictions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività delle partizioni COM+](com--partitions-tasks.md)
</dt> </dl>

 

 



