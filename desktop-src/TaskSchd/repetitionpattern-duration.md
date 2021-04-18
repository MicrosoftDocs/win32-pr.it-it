---
title: Proprietà RepetitionPattern. Duration
description: Per la creazione di script, ottiene o imposta il tempo di ripetizione del modello.
ms.assetid: 41a56414-981b-440a-b51a-228125baf303
keywords:
- Utilità di pianificazione della proprietà Duration
- Utilità di pianificazione proprietà Duration, oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione, proprietà Duration
topic_type:
- apiref
api_name:
- RepetitionPattern.Duration
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51ff18330fd69bb54fdfb489b72f9470f707aed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302012"
---
# <a name="repetitionpatternduration-property"></a><span data-ttu-id="4d984-106">Proprietà RepetitionPattern. Duration</span><span class="sxs-lookup"><span data-stu-id="4d984-106">RepetitionPattern.Duration property</span></span>

<span data-ttu-id="4d984-107">Per la creazione di script, ottiene o imposta il tempo di ripetizione del modello.</span><span class="sxs-lookup"><span data-stu-id="4d984-107">For scripting, gets or sets how long the pattern is repeated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d984-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d984-108">Syntax</span></span>


```VB
RepetitionPattern.Duration As String
```



## <a name="property-value"></a><span data-ttu-id="4d984-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4d984-109">Property value</span></span>

<span data-ttu-id="4d984-110">Tempo di ripetizione del modello.</span><span class="sxs-lookup"><span data-stu-id="4d984-110">How long the pattern is repeated.</span></span> <span data-ttu-id="4d984-111">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="4d984-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="4d984-112">Il tempo minimo consentito è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="4d984-112">The minimum time allowed is one minute.</span></span>

<span data-ttu-id="4d984-113">Se non viene specificato alcun valore per la durata, il modello viene ripetuto per un tempo illimitato.</span><span class="sxs-lookup"><span data-stu-id="4d984-113">If no value is specified for the duration, then the pattern is repeated indefinitely.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d984-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d984-114">Remarks</span></span>

<span data-ttu-id="4d984-115">Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="4d984-115">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="4d984-116">Durante la lettura o la scrittura di codice XML per un'attività, la durata della ripetizione viene specificata nell'elemento [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="4d984-116">When reading or writing XML for a task, the repetition duration is specified in the [**Duration**](taskschedulerschema-duration-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d984-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d984-117">Requirements</span></span>



| <span data-ttu-id="4d984-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d984-118">Requirement</span></span> | <span data-ttu-id="4d984-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4d984-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d984-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d984-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4d984-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d984-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4d984-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d984-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4d984-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d984-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d984-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4d984-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d984-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d984-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d984-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4d984-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d984-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d984-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d984-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d984-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d984-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4d984-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





