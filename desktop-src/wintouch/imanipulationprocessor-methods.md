---
title: Metodi (IInertiaProcessor)
description: Questa sezione contiene i metodi per l'interfaccia IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interfaccia IInertiaProcessor
- Windows Touch, metodi di interfaccia
- inerzia, interfaccia IInertiaProcessor
- Interfaccia IInertiaProcessor, metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300900"
---
# <a name="methods-iinertiaprocessor"></a><span data-ttu-id="2a605-107">Metodi (IInertiaProcessor)</span><span class="sxs-lookup"><span data-stu-id="2a605-107">Methods (IInertiaProcessor)</span></span>

<span data-ttu-id="2a605-108">Questa sezione contiene i metodi per l'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .</span><span class="sxs-lookup"><span data-stu-id="2a605-108">This section contains the methods for the [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) interface.</span></span>



| <span data-ttu-id="2a605-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="2a605-109">Method</span></span>                                                 | <span data-ttu-id="2a605-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a605-110">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a605-111">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2a605-111">**Reset**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | <span data-ttu-id="2a605-112">Inizializza il processore con il timestamp iniziale e riavvia l'inerzia.</span><span class="sxs-lookup"><span data-stu-id="2a605-112">Initializes the processor with initial time stamp and restarts inertia.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="2a605-113">**Processo**</span><span class="sxs-lookup"><span data-stu-id="2a605-113">**Process**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | <span data-ttu-id="2a605-114">Esegue calcoli per il ciclo corrente e può generare l'evento **Delta** o **Completed** a seconda che l'estrapolazione sia stata completata o meno.</span><span class="sxs-lookup"><span data-stu-id="2a605-114">Performs calculations for the current tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span> <span data-ttu-id="2a605-115">Se l'estrapolazione è stata completata al momento precedente, il metodo non è op.</span><span class="sxs-lookup"><span data-stu-id="2a605-115">If extrapolation finished at the previous tick, the method is no-op.</span></span> |
| [<span data-ttu-id="2a605-116">**ProcessTime**</span><span class="sxs-lookup"><span data-stu-id="2a605-116">**ProcessTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | <span data-ttu-id="2a605-117">Esegue calcoli per il segno di selezione specificato e può generare l'evento **Delta** o **Completed** a seconda che l'estrapolazione sia stata completata o meno.</span><span class="sxs-lookup"><span data-stu-id="2a605-117">Performs calculations for the given tick and can raise the **Delta** or **Completed** event depending on whether extrapolation is completed or not.</span></span>                                                                        |
| [<span data-ttu-id="2a605-118">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="2a605-118">**Complete**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | <span data-ttu-id="2a605-119">Termina la manipolazione corrente e arresta l'inerzia del processore di inerzia.</span><span class="sxs-lookup"><span data-stu-id="2a605-119">Finishes the current manipulation and stops inertia on the inertia processor.</span></span>                                                                                                                                              |
| [<span data-ttu-id="2a605-120">**CompleteTime**</span><span class="sxs-lookup"><span data-stu-id="2a605-120">**CompleteTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | <span data-ttu-id="2a605-121">Termina la manipolazione corrente in corrispondenza del segno di selezione specificato, interrompe l'inerzia del processore di inerzia e genera l'evento ManipulationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2a605-121">Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event.</span></span>                                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="2a605-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a605-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a605-123">**IInertiaProcessor**</span><span class="sxs-lookup"><span data-stu-id="2a605-123">**IInertiaProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




