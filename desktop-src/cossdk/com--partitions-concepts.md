---
description: Concetti relativi alle partizioni COM+
ms.assetid: 9fc35bef-ecc1-4764-bf69-ec89560daff4
title: Concetti relativi alle partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 483a34e6186cda8978c1882ed1fdfbe8732f7ec8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483077"
---
# <a name="com-partitions-concepts"></a>Concetti relativi alle partizioni COM+

Negli ambienti di elaborazione in cui è necessario utilizzare diverse versioni o configurazioni di un'applicazione nello stesso computer, è possibile che si verifichino conflitti quando una versione dell'applicazione richiede componenti diversi rispetto all'altra o quando una versione richiede un componente nel computer che non è compatibile con l'altra versione dell'applicazione. In passato, l'unico modo per risolvere questo problema era gestire più computer ed eseguire una versione diversa dell'applicazione in ogni computer. Un approccio di questo tipo è costoso e inefficiente perché aumenta i costi hardware e il sovraccarico amministrativo.

COM+ risolve questo problema fornendo la funzionalità partizioni COM+. È possibile utilizzare le partizioni COM+ per installare versioni diverse di un'applicazione COM+ in un computer ed eseguirle contemporaneamente.

Per comprendere e utilizzare questa funzionalità, vedere gli argomenti seguenti:

-   [Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
-   [Implementazione della partizione](partition-implementation.md)
-   [Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
-   [Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
-   [Limitazioni relative alla progettazione di applicazioni](application-design-restrictions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività partizioni COM+](com--partitions-tasks.md)
</dt> </dl>

 

 



