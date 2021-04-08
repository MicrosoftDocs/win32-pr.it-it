---
title: Metodo ActionCollection. Remove
description: Per la creazione di script, rimuove l'azione specificata dalla raccolta.
ms.assetid: ae1da6a9-5851-4ccb-80dc-75d7a99e7c6a
keywords:
- Rimuovere il metodo Utilità di pianificazione
- Remove Method Utilità di pianificazione, oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, metodo Remove
topic_type:
- apiref
api_name:
- ActionCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e110f870f4f192051b47cb3b65f0ebb41a490708
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742463"
---
# <a name="actioncollectionremove-method"></a><span data-ttu-id="bcf34-106">Metodo ActionCollection. Remove</span><span class="sxs-lookup"><span data-stu-id="bcf34-106">ActionCollection.Remove method</span></span>

<span data-ttu-id="bcf34-107">Per la creazione di script, rimuove l'azione specificata dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="bcf34-107">For scripting, removes the specified action from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcf34-108">Syntax</span></span>


```VB
ActionCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="bcf34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcf34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf34-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="bcf34-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf34-111">Indice dell'azione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="bcf34-111">The index of the action to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf34-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcf34-112">Return value</span></span>

<span data-ttu-id="bcf34-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bcf34-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf34-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcf34-114">Remarks</span></span>

<span data-ttu-id="bcf34-115">Quando si rimuovono elementi, si noti che l'indice per il primo elemento nella raccolta è 1 e l'indice per l'ultimo elemento è il valore della proprietà [**ActionCollection. Count**](actioncollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="bcf34-115">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**ActionCollection.Count**](actioncollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf34-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcf34-116">Requirements</span></span>



| <span data-ttu-id="bcf34-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf34-117">Requirement</span></span> | <span data-ttu-id="bcf34-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bcf34-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf34-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf34-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf34-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcf34-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bcf34-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf34-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf34-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bcf34-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bcf34-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bcf34-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcf34-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bcf34-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bcf34-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf34-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf34-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf34-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf34-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcf34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf34-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bcf34-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="bcf34-129">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="bcf34-129">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





