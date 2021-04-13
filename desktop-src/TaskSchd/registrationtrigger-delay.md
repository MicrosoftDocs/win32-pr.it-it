---
title: Proprietà RegistrationTrigger. Delay
description: Per gli script, ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.
ms.assetid: 33b8f212-66eb-4396-b21f-eeb1a5175efc
keywords:
- Utilità di pianificazione di proprietà delay
- Utilità di pianificazione di proprietà delay, oggetto RegistrationTrigger
- Utilità di pianificazione oggetto RegistrationTrigger, proprietà delay
topic_type:
- apiref
api_name:
- RegistrationTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad86017547ac4476f430e13e2566ddd6d3494226
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518603"
---
# <a name="registrationtriggerdelay-property"></a><span data-ttu-id="38441-106">Proprietà RegistrationTrigger. Delay</span><span class="sxs-lookup"><span data-stu-id="38441-106">RegistrationTrigger.Delay property</span></span>

<span data-ttu-id="38441-107">Per gli script, ottiene o imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="38441-107">For scripting, gets or sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="38441-108">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="38441-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="38441-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38441-109">Syntax</span></span>


```VB
RegistrationTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="38441-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="38441-110">Property value</span></span>

<span data-ttu-id="38441-111">Intervallo di tempo tra il momento in cui il sistema viene registrato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="38441-111">The amount of time between when the system is registered and when the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="38441-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="38441-112">Remarks</span></span>

<span data-ttu-id="38441-113">Durante la lettura o la scrittura di codice XML per un'attività, il ritardo di avvio viene specificato utilizzando l'elemento [**delay**](taskschedulerschema-delay-registrationtriggertype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="38441-113">When reading or writing XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-registrationtriggertype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="38441-114">Se un'attività con un trigger di registrazione ritardata viene registrata e il computer in cui è registrata l'attività viene arrestato o riavviato durante il ritardo, prima dell'esecuzione dell'attività, l'attività non verrà eseguita e il ritardo andrà perso.</span><span class="sxs-lookup"><span data-stu-id="38441-114">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="38441-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38441-115">Requirements</span></span>



| <span data-ttu-id="38441-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38441-116">Requirement</span></span> | <span data-ttu-id="38441-117">Valore</span><span class="sxs-lookup"><span data-stu-id="38441-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38441-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38441-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38441-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38441-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="38441-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38441-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38441-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38441-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38441-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="38441-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="38441-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38441-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38441-124">DLL</span><span class="sxs-lookup"><span data-stu-id="38441-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38441-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38441-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38441-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38441-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38441-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="38441-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





