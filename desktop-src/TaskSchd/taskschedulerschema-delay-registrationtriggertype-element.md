---
title: Elemento Delay (registrationTriggerType)
description: Specifica l'intervallo di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
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
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743778"
---
# <a name="delay-registrationtriggertype-element"></a><span data-ttu-id="e7175-104">Elemento Delay (registrationTriggerType)</span><span class="sxs-lookup"><span data-stu-id="e7175-104">Delay (registrationTriggerType) Element</span></span>

<span data-ttu-id="e7175-105">Specifica l'intervallo di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e7175-105">Specifies the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="e7175-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="e7175-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e7175-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e7175-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="e7175-108">L'elemento **delay** viene definito dal tipo complesso [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e7175-108">The **Delay** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e7175-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e7175-109">Parent element</span></span>



| <span data-ttu-id="e7175-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="e7175-110">Element</span></span>                                                                                     | <span data-ttu-id="e7175-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e7175-111">Derived from</span></span>                                                                               | <span data-ttu-id="e7175-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7175-112">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e7175-113">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="e7175-113">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="e7175-114">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="e7175-114">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="e7175-115">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="e7175-115">Specifies a trigger that starts a task when the task is registered.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7175-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7175-116">Remarks</span></span>

<span data-ttu-id="e7175-117">Per lo sviluppo di script, il ritardo del trigger di registrazione viene specificato tramite la proprietà [**RegistrationTrigger. Delay**](registrationtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="e7175-117">For scripting development, the registration trigger delay is specified using the [**RegistrationTrigger.Delay**](registrationtrigger-delay.md) property.</span></span>

<span data-ttu-id="e7175-118">Per lo sviluppo in C++, il ritardo del trigger di registrazione viene specificato con la proprietà [**IRegistrationTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="e7175-118">For C++ development, the registration trigger delay is specified using the [**IRegistrationTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e7175-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="e7175-119">Examples</span></span>

<span data-ttu-id="e7175-120">Il codice XML seguente definisce un ritardo del trigger di registrazione che consente un ritardo di 5 minuti tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e7175-120">The following XML defines a registration trigger delay that allows a 5 minute delay between when the task is registered and when the task is started.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="e7175-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7175-121">Requirements</span></span>



| <span data-ttu-id="e7175-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7175-122">Requirement</span></span> | <span data-ttu-id="e7175-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e7175-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7175-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7175-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e7175-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7175-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7175-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7175-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e7175-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e7175-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7175-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7175-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7175-129">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e7175-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e7175-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e7175-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





