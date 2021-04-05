---
title: Proprietà BootTrigger. Delay
description: Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto BootTrigger
- Utilità di pianificazione oggetto BootTrigger, proprietà delay
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120430"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="21439-106">Proprietà BootTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="21439-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="21439-107">Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="21439-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="21439-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21439-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="21439-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="21439-109">Property value</span></span>

<span data-ttu-id="21439-110">Valore che indica la quantità di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="21439-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="21439-111">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="21439-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="21439-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="21439-112">Remarks</span></span>

<span data-ttu-id="21439-113">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, il ritardo di avvio viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-boottriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="21439-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="21439-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21439-114">Requirements</span></span>



| <span data-ttu-id="21439-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="21439-115">Requirement</span></span> | <span data-ttu-id="21439-116">Valore</span><span class="sxs-lookup"><span data-stu-id="21439-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21439-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21439-117">Minimum supported client</span></span><br/> | <span data-ttu-id="21439-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="21439-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="21439-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21439-119">Minimum supported server</span></span><br/> | <span data-ttu-id="21439-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="21439-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21439-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="21439-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="21439-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21439-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21439-123">DLL</span><span class="sxs-lookup"><span data-stu-id="21439-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21439-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21439-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21439-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21439-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21439-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="21439-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="21439-127">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="21439-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





