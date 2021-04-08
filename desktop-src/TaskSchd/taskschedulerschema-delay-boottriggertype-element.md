---
title: Elemento Delay (bootTriggerType)
description: Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
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
ms.openlocfilehash: 1ab28da8e9c739d3deff52572fe6a5d37f862119
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964957"
---
# <a name="delay-boottriggertype-element"></a><span data-ttu-id="ce034-104">Elemento Delay (bootTriggerType)</span><span class="sxs-lookup"><span data-stu-id="ce034-104">Delay (bootTriggerType) Element</span></span>

<span data-ttu-id="ce034-105">Specifica l'intervallo di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="ce034-105">Specifies the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="ce034-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="ce034-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="ce034-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="ce034-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="ce034-108">L'elemento **delay** viene definito dal tipo complesso [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ce034-108">The **Delay** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce034-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="ce034-109">Parent element</span></span>



| <span data-ttu-id="ce034-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ce034-110">Element</span></span>                                                                     | <span data-ttu-id="ce034-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="ce034-111">Derived from</span></span>                                                               | <span data-ttu-id="ce034-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce034-112">Description</span></span>                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="ce034-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="ce034-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md) | [<span data-ttu-id="ce034-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="ce034-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md) | <span data-ttu-id="ce034-115">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="ce034-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce034-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce034-116">Remarks</span></span>

<span data-ttu-id="ce034-117">Per lo sviluppo di script, il ritardo del trigger dell'evento viene specificato dalla proprietà [**BootTrigger. Delay**](boottrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="ce034-117">For script development, the event trigger delay is specified by the [**BootTrigger.Delay**](boottrigger-delay.md) property.</span></span>

<span data-ttu-id="ce034-118">Per lo sviluppo in C++, il ritardo del trigger dell'evento viene specificato dalla proprietà [**IBootTrigger::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="ce034-118">For C++ development, the event trigger delay is specified by the [**IBootTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce034-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce034-119">Requirements</span></span>



| <span data-ttu-id="ce034-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce034-120">Requirement</span></span> | <span data-ttu-id="ce034-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ce034-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce034-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce034-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce034-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce034-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce034-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce034-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce034-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce034-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce034-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce034-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce034-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ce034-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ce034-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="ce034-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





