---
title: Proprietà ActionCollection. Context
description: Per gli script, ottiene o imposta l'identificatore dell'entità per l'attività.
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- Utilità di pianificazione della proprietà di contesto
- Utilità di pianificazione di proprietà di contesto, oggetto ActionCollection
- Utilità di pianificazione oggetto ActionCollection, proprietà di contesto
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302017"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="94b27-106">Proprietà ActionCollection. Context</span><span class="sxs-lookup"><span data-stu-id="94b27-106">ActionCollection.Context property</span></span>

<span data-ttu-id="94b27-107">Per gli script, ottiene o imposta l'identificatore dell'entità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="94b27-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="94b27-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="94b27-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="94b27-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="94b27-109">Property value</span></span>

<span data-ttu-id="94b27-110">Identificatore dell'entità per l'attività.</span><span class="sxs-lookup"><span data-stu-id="94b27-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="94b27-111">L'identificatore specificato qui deve corrispondere all'identificatore specificato nella proprietà ID dell'interfaccia IPrincipal che definisce l'entità.</span><span class="sxs-lookup"><span data-stu-id="94b27-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="94b27-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94b27-112">Requirements</span></span>



| <span data-ttu-id="94b27-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="94b27-113">Requirement</span></span> | <span data-ttu-id="94b27-114">Valore</span><span class="sxs-lookup"><span data-stu-id="94b27-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94b27-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94b27-115">Minimum supported client</span></span><br/> | <span data-ttu-id="94b27-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94b27-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="94b27-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="94b27-117">Minimum supported server</span></span><br/> | <span data-ttu-id="94b27-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94b27-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94b27-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="94b27-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="94b27-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="94b27-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="94b27-121">DLL</span><span class="sxs-lookup"><span data-stu-id="94b27-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94b27-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94b27-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94b27-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94b27-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94b27-124">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="94b27-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="94b27-125">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="94b27-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





