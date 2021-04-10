---
title: Proprietà CounterItem. Selected
description: Recupera o imposta un valore che indica se il contatore è selezionato.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Proprietà selezionata SysMon
- Proprietà selezionata SysMon, oggetto CounterItem
- Oggetto CounterItem SysMon, proprietà selezionata
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964323"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="51efd-106">Proprietà CounterItem. Selected</span><span class="sxs-lookup"><span data-stu-id="51efd-106">CounterItem.Selected property</span></span>

<span data-ttu-id="51efd-107">Recupera o imposta un valore che indica se il contatore è selezionato.</span><span class="sxs-lookup"><span data-stu-id="51efd-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="51efd-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="51efd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51efd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51efd-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="51efd-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="51efd-110">Property value</span></span>

<span data-ttu-id="51efd-111">True se il contatore è selezionato; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="51efd-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="51efd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="51efd-112">Remarks</span></span>

<span data-ttu-id="51efd-113">È possibile selezionare uno o più contatori dalla raccolta di contatori.</span><span class="sxs-lookup"><span data-stu-id="51efd-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="51efd-114">Selezionando un contatore, viene selezionato il contatore nella legenda, il contatore viene reso visibile nella legenda e viene generato un evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .</span><span class="sxs-lookup"><span data-stu-id="51efd-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="51efd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51efd-115">Requirements</span></span>



| <span data-ttu-id="51efd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51efd-116">Requirement</span></span> | <span data-ttu-id="51efd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="51efd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51efd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51efd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51efd-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51efd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51efd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51efd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51efd-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51efd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51efd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="51efd-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51efd-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="51efd-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51efd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51efd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51efd-125">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="51efd-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





