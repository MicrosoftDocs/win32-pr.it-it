---
title: Elemento Delay (logonTriggerType)
description: Intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.
ms.assetid: daab29f7-5d05-4e6d-a0c0-7b83b4d0b941
keywords:
- Utilità di pianificazione elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a820bad3d68cfb0a697f795a9fd7326c9e52abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478904"
---
# <a name="delay-logontriggertype-element"></a><span data-ttu-id="53006-104">Elemento Delay (logonTriggerType)</span><span class="sxs-lookup"><span data-stu-id="53006-104">Delay (logonTriggerType) Element</span></span>

<span data-ttu-id="53006-105">Intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="53006-105">Amount of time between when the user logs on and when the task is started.</span></span> <span data-ttu-id="53006-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="53006-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="53006-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="53006-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="53006-108">L'elemento **delay** viene definito dal tipo complesso [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="53006-108">The **Delay** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="53006-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="53006-109">Parent element</span></span>



| <span data-ttu-id="53006-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="53006-110">Element</span></span>                                                                       | <span data-ttu-id="53006-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="53006-111">Derived from</span></span>                                                                 | <span data-ttu-id="53006-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53006-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="53006-113">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="53006-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="53006-114">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="53006-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="53006-115">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="53006-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="53006-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="53006-116">Remarks</span></span>

<span data-ttu-id="53006-117">Per lo sviluppo di script, il ritardo del trigger LOGON viene specificato mediante la proprietà [**LogonTrigger. Delay**](logontrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="53006-117">For scripting development, the logon trigger delay is specified using the [**LogonTrigger.Delay**](logontrigger-delay.md) property.</span></span>

<span data-ttu-id="53006-118">Per lo sviluppo in C++, l'identificatore utente per il trigger LOGON viene specificato con la proprietà [**ILogonTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="53006-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="53006-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53006-119">Requirements</span></span>



| <span data-ttu-id="53006-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53006-120">Requirement</span></span> | <span data-ttu-id="53006-121">Valore</span><span class="sxs-lookup"><span data-stu-id="53006-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53006-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53006-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53006-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53006-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53006-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53006-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53006-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53006-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53006-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53006-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53006-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="53006-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="53006-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="53006-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





