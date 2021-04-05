---
title: Enumerazione delle attività
description: Utilità di pianificazione 1,0 fornisce un oggetto di enumerazione per l'enumerazione delle attività nella cartella delle attività pianificate.
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- Enumerazione delle attività Utilità di pianificazione
- Enumerazione delle attività Utilità di pianificazione, descritta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045009"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="b2ae1-105">Enumerazione delle attività</span><span class="sxs-lookup"><span data-stu-id="b2ae1-105">Enumerating Tasks</span></span>

<span data-ttu-id="b2ae1-106">Utilità di pianificazione 1,0 fornisce un oggetto di enumerazione per l'enumerazione delle attività nella [*cartella delle attività pianificate*](s.md).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="b2ae1-107">Per un computer Windows Server 2003, Windows XP o Windows 2000 per creare, monitorare o controllare le attività in un computer con Windows Vista, è necessario completare alcune operazioni sul computer Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2ae1-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="b2ae1-108">Per altre informazioni, vedere [Tasks](tasks.md) (Attività).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="b2ae1-109">Utilizzo dell'oggetto Enumeration</span><span class="sxs-lookup"><span data-stu-id="b2ae1-109">Using the Enumeration Object</span></span>

<span data-ttu-id="b2ae1-110">L'interfaccia [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) di questo oggetto fornisce i metodi per enumerare le attività nella cartella, reimpostando la sequenza di enumerazione sull'inizio dell'elenco, ignorando le attività e creando una copia dell'oggetto di enumerazione corrente per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="b2ae1-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="b2ae1-111">Per informazioni sull'enumerazione delle attività nella cartella delle attività pianificate, vedere [**IEnumWorkItems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="b2ae1-112">Per informazioni sulla reimpostazione dell'enumerazione all'inizio dell'elenco, vedere [**IEnumWorkItems:: Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="b2ae1-113">Per informazioni sulle attività ignorate, vedere [**IEnumWorkItems:: Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="b2ae1-114">Per informazioni su come creare una copia dell'oggetto di enumerazione corrente, vedere [**IEnumWorkItems:: Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span><span class="sxs-lookup"><span data-stu-id="b2ae1-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="b2ae1-115">Per un esempio di enumerazione delle attività nella cartella delle attività pianificate, vedere [esempio di enumerazione](enumerating-tasks-example.md)delle attività.</span><span class="sxs-lookup"><span data-stu-id="b2ae1-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2ae1-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2ae1-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b2ae1-117">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b2ae1-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2ae1-118">Informazioni sull'attività Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="b2ae1-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




