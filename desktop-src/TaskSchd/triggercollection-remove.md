---
title: TriggerCollection. Remove (metodo)
description: Per gli script, rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.
ms.assetid: 30dccf16-2b4c-4776-9c19-f82ddd859d45
keywords:
- trigger Utilità di pianificazione, rimozione
- Rimuovere il metodo Utilità di pianificazione
- Rimuovere il metodo Utilità di pianificazione, oggetto TriggerCollection
- TriggerCollection, oggetto Utilità di pianificazione, Remove (metodo)
topic_type:
- apiref
api_name:
- TriggerCollection.Remove
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e84e57b28db9b08fd7e93e85fb7bc35f60647
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340612"
---
# <a name="triggercollectionremove-method"></a><span data-ttu-id="67f7c-107">TriggerCollection. Remove (metodo)</span><span class="sxs-lookup"><span data-stu-id="67f7c-107">TriggerCollection.Remove method</span></span>

<span data-ttu-id="67f7c-108">Per gli script, rimuove il trigger specificato dalla raccolta di trigger utilizzati dall'attività.</span><span class="sxs-lookup"><span data-stu-id="67f7c-108">For scripting, removes the specified trigger from the collection of triggers used by the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f7c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67f7c-109">Syntax</span></span>


```VB
TriggerCollection.Remove( _
  ByVal index _
)
```



## <a name="parameters"></a><span data-ttu-id="67f7c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="67f7c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f7c-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="67f7c-111">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f7c-112">Indice del trigger da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="67f7c-112">The index of the trigger to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f7c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67f7c-113">Return value</span></span>

<span data-ttu-id="67f7c-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="67f7c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f7c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="67f7c-115">Remarks</span></span>

<span data-ttu-id="67f7c-116">Quando si rimuovono elementi, si noti che l'indice per il primo elemento nella raccolta è 1 e l'indice per l'ultimo elemento è il valore della proprietà [**TriggerCollection. Count**](triggercollection-count.md) .</span><span class="sxs-lookup"><span data-stu-id="67f7c-116">When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the [**TriggerCollection.Count**](triggercollection-count.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f7c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67f7c-117">Requirements</span></span>



| <span data-ttu-id="67f7c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f7c-118">Requirement</span></span> | <span data-ttu-id="67f7c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="67f7c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f7c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67f7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="67f7c-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67f7c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67f7c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67f7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="67f7c-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67f7c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67f7c-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="67f7c-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="67f7c-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67f7c-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67f7c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="67f7c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f7c-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f7c-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67f7c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67f7c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f7c-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="67f7c-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





