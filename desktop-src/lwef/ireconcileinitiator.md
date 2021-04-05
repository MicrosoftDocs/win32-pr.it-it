---
title: Interfaccia IReconcileInitiator
description: Espone i metodi che forniscono il riconciliatore della valigetta con i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una versione specifica di un documento. L'Initiator è responsabile dell'implementazione di questa interfaccia.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IReconcileInitiator
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IReconcileInitiator, descritte
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741599"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="5297f-106">Interfaccia IReconcileInitiator</span><span class="sxs-lookup"><span data-stu-id="5297f-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="5297f-107">Espone i metodi che forniscono il riconciliatore della valigetta con i mezzi per notificare all'iniziatore lo stato di avanzamento, per impostare un oggetto di terminazione e per richiedere una versione specifica di un documento.</span><span class="sxs-lookup"><span data-stu-id="5297f-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="5297f-108">L'Initiator è responsabile dell'implementazione di questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5297f-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="5297f-109">Membri</span><span class="sxs-lookup"><span data-stu-id="5297f-109">Members</span></span>

<span data-ttu-id="5297f-110">L'interfaccia **IReconcileInitiator** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5297f-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5297f-111">**IReconcileInitiator** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5297f-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="5297f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5297f-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5297f-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="5297f-113">Methods</span></span>

<span data-ttu-id="5297f-114">L'interfaccia **IReconcileInitiator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5297f-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="5297f-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="5297f-115">Method</span></span>                                                                 | <span data-ttu-id="5297f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5297f-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5297f-117">**SetAbortCallback**</span><span class="sxs-lookup"><span data-stu-id="5297f-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="5297f-118">Imposta l'oggetto tramite il quale l'iniziatore può terminare in modo asincrono una riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="5297f-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="5297f-119">Un riconciliatore di valigetta imposta in genere questo oggetto per le riconciliazioni che sono lunghe o coinvolgono l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5297f-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="5297f-120">**SetProgressFeedback**</span><span class="sxs-lookup"><span data-stu-id="5297f-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="5297f-121">Indica la quantità di avanzamento apportata dal riconciliatore della valigetta verso il completamento della riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="5297f-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="5297f-122">La quantità è una frazione e viene calcolata come quoziente dei parametri *ulProgress* e *ulProgressMax* .</span><span class="sxs-lookup"><span data-stu-id="5297f-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="5297f-123">I riconciliatori devono chiamare questo metodo periodicamente durante il processo di riconciliazione.</span><span class="sxs-lookup"><span data-stu-id="5297f-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="5297f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5297f-124">Requirements</span></span>



| <span data-ttu-id="5297f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5297f-125">Requirement</span></span> | <span data-ttu-id="5297f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5297f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5297f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5297f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5297f-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5297f-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5297f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5297f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5297f-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5297f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5297f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5297f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5297f-132"><dt>Shell32.dll (versione 4,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="5297f-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

