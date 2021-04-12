---
title: Proprietà ComHandlerAction. Data
description: Per gli script, ottiene o imposta dati aggiuntivi associati al gestore.
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- Utilità di pianificazione proprietà dati
- Utilità di pianificazione proprietà dati, oggetto ComHandlerAction
- Utilità di pianificazione oggetto ComHandlerAction, proprietà Data
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400860"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="e2217-106">Proprietà ComHandlerAction. Data</span><span class="sxs-lookup"><span data-stu-id="e2217-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="e2217-107">Per gli script, ottiene o imposta dati aggiuntivi associati al gestore.</span><span class="sxs-lookup"><span data-stu-id="e2217-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2217-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2217-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="e2217-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e2217-109">Property value</span></span>

<span data-ttu-id="e2217-110">Argomenti necessari per il gestore.</span><span class="sxs-lookup"><span data-stu-id="e2217-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2217-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2217-111">Remarks</span></span>

<span data-ttu-id="e2217-112">Durante la lettura o la scrittura di codice XML, i dati di un gestore COM vengono specificati nell'elemento [**dati**](taskschedulerschema-data-comhandlertype-element.md) dello schema di utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e2217-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2217-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2217-113">Requirements</span></span>



| <span data-ttu-id="e2217-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2217-114">Requirement</span></span> | <span data-ttu-id="e2217-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e2217-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2217-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2217-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2217-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2217-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2217-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2217-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2217-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2217-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2217-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e2217-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2217-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2217-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2217-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e2217-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2217-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2217-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2217-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2217-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2217-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e2217-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e2217-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="e2217-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





