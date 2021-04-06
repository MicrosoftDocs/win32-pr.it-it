---
title: Proprietà IdleSettings. IdleDuration
description: Per gli script, ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.
ms.assetid: 32b9a14e-e37e-4e3a-81eb-041387f2017b
keywords:
- Utilità di pianificazione proprietà IdleDuration
- Utilità di pianificazione proprietà IdleDuration, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, Proprietà IdleDuration
topic_type:
- apiref
api_name:
- IdleSettings.IdleDuration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6eeed4fef540b3a9e13d0f52e3ce1934cb9e220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742455"
---
# <a name="idlesettingsidleduration-property"></a><span data-ttu-id="a97e4-106">Proprietà IdleSettings. IdleDuration</span><span class="sxs-lookup"><span data-stu-id="a97e4-106">IdleSettings.IdleDuration property</span></span>

<span data-ttu-id="a97e4-107">Per gli script, ottiene o imposta un valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a97e4-107">For scripting, gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span>

## <a name="syntax"></a><span data-ttu-id="a97e4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a97e4-108">Syntax</span></span>


```VB
IdleSettings.IdleDuration As String
```



## <a name="property-value"></a><span data-ttu-id="a97e4-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a97e4-109">Property value</span></span>

<span data-ttu-id="a97e4-110">Valore che indica la quantità di tempo in cui il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="a97e4-110">A value that indicates the amount of time that the computer must be in an idle state before the task is run).</span></span> <span data-ttu-id="a97e4-111">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="a97e4-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="a97e4-112">Il valore minimo è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="a97e4-112">The minimum value is one minute.</span></span> <span data-ttu-id="a97e4-113">Se questo valore è **null**, il ritardo verrà impostato sul valore predefinito di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a97e4-113">If this value is **NULL**, then the delay will be set to the default of 10 minutes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a97e4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a97e4-114">Remarks</span></span>

<span data-ttu-id="a97e4-115">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="a97e4-115">When reading or writing XML for a task, this setting is specified in the [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="a97e4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a97e4-116">Requirements</span></span>



| <span data-ttu-id="a97e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a97e4-117">Requirement</span></span> | <span data-ttu-id="a97e4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a97e4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a97e4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a97e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a97e4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a97e4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a97e4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a97e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a97e4-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a97e4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a97e4-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a97e4-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a97e4-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a97e4-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a97e4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a97e4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a97e4-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a97e4-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a97e4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a97e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97e4-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="a97e4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a97e4-129">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="a97e4-129">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





