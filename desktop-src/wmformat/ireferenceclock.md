---
title: Interfaccia IReferenceClock
description: L'interfaccia IReferenceClock fornisce l'accesso a un clock esterno. Questa interfaccia viene fornita per consentire la sincronizzazione di tutte le routine di rendering con lo stesso clock. Questa interfaccia può essere ottenuta da un oggetto Reader.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Formato Windows Media Interface IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, descritto
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299828"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="d534f-106">Interfaccia IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="d534f-106">IReferenceClock interface</span></span>

<span data-ttu-id="d534f-107">L'interfaccia **IReferenceClock** fornisce l'accesso a un clock esterno.</span><span class="sxs-lookup"><span data-stu-id="d534f-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="d534f-108">Questa interfaccia viene fornita per consentire la sincronizzazione di tutte le routine di rendering con lo stesso clock.</span><span class="sxs-lookup"><span data-stu-id="d534f-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="d534f-109">Questa interfaccia può essere ottenuta da un oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="d534f-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="d534f-110">Membri</span><span class="sxs-lookup"><span data-stu-id="d534f-110">Members</span></span>

<span data-ttu-id="d534f-111">L'interfaccia **IReferenceClock** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d534f-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d534f-112">**IReferenceClock** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d534f-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="d534f-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="d534f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d534f-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="d534f-114">Methods</span></span>

<span data-ttu-id="d534f-115">L'interfaccia **IReferenceClock** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d534f-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="d534f-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="d534f-116">Method</span></span>                                                   | <span data-ttu-id="d534f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d534f-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="d534f-118">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="d534f-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="d534f-119">Non implementato da questo SDK.</span><span class="sxs-lookup"><span data-stu-id="d534f-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="d534f-120">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="d534f-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="d534f-121">Richiede una notifica asincrona che è trascorso un periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d534f-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="d534f-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="d534f-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="d534f-123">Recupera l'ora di riferimento corrente.</span><span class="sxs-lookup"><span data-stu-id="d534f-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="d534f-124">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="d534f-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="d534f-125">Annulla una richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="d534f-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="d534f-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d534f-126">Remarks</span></span>

<span data-ttu-id="d534f-127">Per informazioni su altre interfacce che possono essere ottenute usando il metodo QueryInterface di questa interfaccia, vedere oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="d534f-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="d534f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d534f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d534f-129">**Interfacce**</span><span class="sxs-lookup"><span data-stu-id="d534f-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

