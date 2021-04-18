---
title: Oggetto TaskNamedValuePair
description: Oggetto di scripting utilizzato per creare una coppia nome-valore in cui il nome è associato al valore.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Utilità di pianificazione oggetto TaskNamedValuePair
- Oggetto TaskNamedValuePair Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301154"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="641b8-105">Oggetto TaskNamedValuePair</span><span class="sxs-lookup"><span data-stu-id="641b8-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="641b8-106">Oggetto di scripting utilizzato per creare una coppia nome-valore in cui il nome è associato al valore.</span><span class="sxs-lookup"><span data-stu-id="641b8-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="641b8-107">Membri</span><span class="sxs-lookup"><span data-stu-id="641b8-107">Members</span></span>

<span data-ttu-id="641b8-108">L'oggetto **TaskNamedValuePair** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="641b8-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="641b8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="641b8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="641b8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="641b8-110">Properties</span></span>

<span data-ttu-id="641b8-111">L'oggetto **TaskNamedValuePair** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="641b8-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="641b8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="641b8-112">Property</span></span>                                             | <span data-ttu-id="641b8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="641b8-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="641b8-114">**Nome**</span><span class="sxs-lookup"><span data-stu-id="641b8-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="641b8-115">Ottiene o imposta il nome associato a un valore in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="641b8-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="641b8-116">**Valore**</span><span class="sxs-lookup"><span data-stu-id="641b8-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="641b8-117">Ottiene o imposta il valore associato a un nome in una coppia nome-valore.</span><span class="sxs-lookup"><span data-stu-id="641b8-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="641b8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="641b8-118">Remarks</span></span>

<span data-ttu-id="641b8-119">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata una coppia nome-valore utilizzando l'elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="641b8-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="641b8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="641b8-120">Requirements</span></span>



| <span data-ttu-id="641b8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="641b8-121">Requirement</span></span> | <span data-ttu-id="641b8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="641b8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="641b8-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="641b8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="641b8-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="641b8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="641b8-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="641b8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="641b8-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="641b8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="641b8-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="641b8-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="641b8-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="641b8-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="641b8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="641b8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="641b8-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="641b8-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="641b8-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="641b8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="641b8-132">**TaskNamedValueCollection**</span><span class="sxs-lookup"><span data-stu-id="641b8-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





