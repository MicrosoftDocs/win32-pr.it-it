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
# <a name="com-partitions-concepts"></a><span data-ttu-id="08953-103">Concetti relativi alle partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="08953-103">COM+ Partitions Concepts</span></span>

<span data-ttu-id="08953-104">Negli ambienti di elaborazione in cui è necessario utilizzare diverse versioni o configurazioni di un'applicazione nello stesso computer, è possibile che si verifichino conflitti quando una versione dell'applicazione richiede componenti diversi rispetto all'altra o quando una versione richiede un componente nel computer che non è compatibile con l'altra versione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="08953-104">In computing environments where it's necessary to use different versions or configurations of an application on the same computer, conflicts can arise when one version of the application requires different components than the other or when one version requires a component on the computer that is incompatible with the other version of the application.</span></span> <span data-ttu-id="08953-105">In passato, l'unico modo per risolvere questo problema era gestire più computer ed eseguire una versione diversa dell'applicazione in ogni computer.</span><span class="sxs-lookup"><span data-stu-id="08953-105">In the past, the only way to solve this problem was to maintain multiple computers and run a different version of the application on each computer.</span></span> <span data-ttu-id="08953-106">Un approccio di questo tipo è costoso e inefficiente perché aumenta i costi hardware e il sovraccarico amministrativo.</span><span class="sxs-lookup"><span data-stu-id="08953-106">Such an approach is costly and inefficient because it increases hardware costs and administrative overhead.</span></span>

<span data-ttu-id="08953-107">COM+ risolve questo problema fornendo la funzionalità partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="08953-107">COM+ solves this problem by providing the COM+ partitions feature.</span></span> <span data-ttu-id="08953-108">È possibile utilizzare le partizioni COM+ per installare versioni diverse di un'applicazione COM+ in un computer ed eseguirle contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="08953-108">You can use COM+ partitions to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="08953-109">Per comprendere e utilizzare questa funzionalità, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="08953-109">To understand and use this feature, see the following topics:</span></span>

-   [<span data-ttu-id="08953-110">Che cosa sono le partizioni COM+?</span><span class="sxs-lookup"><span data-stu-id="08953-110">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
-   [<span data-ttu-id="08953-111">Implementazione della partizione</span><span class="sxs-lookup"><span data-stu-id="08953-111">Partition Implementation</span></span>](partition-implementation.md)
-   [<span data-ttu-id="08953-112">Registrazione e attivazione di componenti nelle partizioni</span><span class="sxs-lookup"><span data-stu-id="08953-112">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
-   [<span data-ttu-id="08953-113">Componenti e partizioni in coda COM+</span><span class="sxs-lookup"><span data-stu-id="08953-113">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
-   [<span data-ttu-id="08953-114">Limitazioni relative alla progettazione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="08953-114">Application Design Restrictions</span></span>](application-design-restrictions.md)

## <a name="related-topics"></a><span data-ttu-id="08953-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08953-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08953-116">Attività partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="08953-116">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)
</dt> </dl>

 

 



