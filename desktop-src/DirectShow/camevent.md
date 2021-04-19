---
description: La classe CAMEvent è un wrapper per gli eventi di reimpostazione manuale e ripristino automatico.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326578"
---
# <a name="camevent-class"></a><span data-ttu-id="bb0e5-103">Classe CAMEvent</span><span class="sxs-lookup"><span data-stu-id="bb0e5-103">CAMEvent class</span></span>

![gerarchia di classi CamEvent](images/util06.png)

<span data-ttu-id="bb0e5-105">La classe **CAMEvent** è un wrapper per gli eventi di reimpostazione manuale e ripristino automatico.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="bb0e5-106">Questa classe fornisce un modo pratico per gestire gli eventi, anziché chiamare funzioni quali [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span><span class="sxs-lookup"><span data-stu-id="bb0e5-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="bb0e5-107">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="bb0e5-107">Protected Member Variables</span></span>                          | <span data-ttu-id="bb0e5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb0e5-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="bb0e5-109">**\_hEvent m**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="bb0e5-110">Handle di evento.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="bb0e5-111">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="bb0e5-111">Public Methods</span></span>                                      | <span data-ttu-id="bb0e5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb0e5-112">Description</span></span>                                                     |
| [<span data-ttu-id="bb0e5-113">**CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="bb0e5-114">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="bb0e5-115">**~ CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="bb0e5-116">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="bb0e5-117">**Controllo**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="bb0e5-118">Verifica se l'evento è impostato, senza bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="bb0e5-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="bb0e5-120">Imposta lo stato dell'evento su non segnalato.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="bb0e5-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="bb0e5-122">Segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="bb0e5-123">**Attesa**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="bb0e5-124">Si blocca fino a quando l'evento non viene segnalato o fino a quando non si verifica un timeout.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="bb0e5-125">Operatori</span><span class="sxs-lookup"><span data-stu-id="bb0e5-125">Operators</span></span>                                           | <span data-ttu-id="bb0e5-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb0e5-126">Description</span></span>                                                     |
| [<span data-ttu-id="bb0e5-127">**HANDLE operatore**</span><span class="sxs-lookup"><span data-stu-id="bb0e5-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="bb0e5-128">Recupera l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bb0e5-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="bb0e5-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb0e5-129">Requirements</span></span>



| <span data-ttu-id="bb0e5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb0e5-130">Requirement</span></span> | <span data-ttu-id="bb0e5-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bb0e5-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0e5-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb0e5-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bb0e5-133"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb0e5-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bb0e5-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="bb0e5-134">Library</span></span><br/> | <dl> <span data-ttu-id="bb0e5-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bb0e5-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

