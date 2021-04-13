---
title: Proprietà LogonTrigger. Delay
description: Per lo scripting, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.
ms.assetid: 42198357-18e9-4fff-a8bf-f2da36148dc8
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto LogonTrigger
- Utilità di pianificazione oggetto LogonTrigger, proprietà delay
topic_type:
- apiref
api_name:
- LogonTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce709b5095ffaeb9fdb5a4532f496ffa34c24e5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400349"
---
# <a name="logontriggerdelay-property"></a><span data-ttu-id="ce011-106">Proprietà LogonTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="ce011-106">LogonTrigger.Delay property</span></span>

<span data-ttu-id="ce011-107">Per lo scripting, ottiene o imposta un valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ce011-107">For scripting, gets or sets a value that indicates the amount of time between when the user logs on and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce011-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce011-108">Syntax</span></span>


```VB
LogonTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="ce011-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ce011-109">Property value</span></span>

<span data-ttu-id="ce011-110">Valore che indica l'intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ce011-110">A value that indicates the amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="ce011-111">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="ce011-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce011-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce011-112">Remarks</span></span>

<span data-ttu-id="ce011-113">Durante la lettura o la scrittura di codice XML per un'attività, il ritardo del trigger LOGON viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-logontriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ce011-113">When reading or writing XML for a task, the logon trigger delay is specified using the [**Delay**](taskschedulerschema-delay-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce011-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce011-114">Requirements</span></span>



| <span data-ttu-id="ce011-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce011-115">Requirement</span></span> | <span data-ttu-id="ce011-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ce011-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce011-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce011-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce011-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce011-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce011-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce011-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce011-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce011-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce011-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ce011-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce011-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce011-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce011-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ce011-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce011-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce011-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce011-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce011-126">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="ce011-126">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="ce011-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ce011-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





