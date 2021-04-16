---
title: Tipo complesso triggerBaseType
description: Definisce l'attributo, gli elementi figlio di base e le informazioni di sequenziazione per tutti i tipi complessi di trigger.
ms.assetid: 1a2d004a-6f52-42b7-b0d0-ace8d27e9166
keywords:
- Utilità di pianificazione di tipo complesso triggerBaseType
topic_type:
- apiref
api_name:
- triggerBaseType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 56602e4a7e6599b7b756ff6bc109376dddc63ac0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341293"
---
# <a name="triggerbasetype-complex-type"></a><span data-ttu-id="5dc24-104">Tipo complesso triggerBaseType</span><span class="sxs-lookup"><span data-stu-id="5dc24-104">triggerBaseType Complex Type</span></span>

<span data-ttu-id="5dc24-105">Definisce l'attributo, gli elementi figlio di base e le informazioni di sequenziazione per tutti i tipi complessi di trigger.</span><span class="sxs-lookup"><span data-stu-id="5dc24-105">Defines the attribute, base child elements, and sequencing information for all trigger complex types.</span></span>

``` syntax
<xs:complexType name="triggerBaseType"
    abstract="true"
>
    <xs:sequence>
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="EndBoundary"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Repetition"
            type="repetitionType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5dc24-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5dc24-106">Child elements</span></span>



| <span data-ttu-id="5dc24-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5dc24-107">Element</span></span>                                                                                      | <span data-ttu-id="5dc24-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dc24-108">Type</span></span>                                                                     | <span data-ttu-id="5dc24-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc24-109">Description</span></span>                                                                                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dc24-110">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="5dc24-110">**Enabled**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="5dc24-111">boolean</span><span class="sxs-lookup"><span data-stu-id="5dc24-111">boolean</span></span>                                                                  | <span data-ttu-id="5dc24-112">Specifica che il trigger è abilitato.</span><span class="sxs-lookup"><span data-stu-id="5dc24-112">Specifies that the trigger is enabled.</span></span><br/>                                                                      |
| [<span data-ttu-id="5dc24-113">**EndBoundary**</span><span class="sxs-lookup"><span data-stu-id="5dc24-113">**EndBoundary**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="5dc24-114">dateTime</span><span class="sxs-lookup"><span data-stu-id="5dc24-114">dateTime</span></span>                                                                 | <span data-ttu-id="5dc24-115">Data e ora in cui il trigger viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="5dc24-115">The date and time when the trigger is deactivated.</span></span><br/>                                                          |
| [<span data-ttu-id="5dc24-116">**ExecutionTimeLimit**</span><span class="sxs-lookup"><span data-stu-id="5dc24-116">**ExecutionTimeLimit**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="5dc24-117">duration</span><span class="sxs-lookup"><span data-stu-id="5dc24-117">duration</span></span>                                                                 | <span data-ttu-id="5dc24-118">Consente di specificare l'intervallo di avvio dell'attività da parte del trigger.</span><span class="sxs-lookup"><span data-stu-id="5dc24-118">Specifies the interval when the trigger can start the task.</span></span><br/>                                                 |
| [<span data-ttu-id="5dc24-119">**Ripetizione**</span><span class="sxs-lookup"><span data-stu-id="5dc24-119">**Repetition**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="5dc24-120">**repetitionType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-120">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="5dc24-121">Specifica la frequenza con cui viene eseguita l'attività e il tempo durante il quale il modello di ripetizione viene ripetuto una volta attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="5dc24-121">Specifies how often the task is run and how long the repetition pattern is repeated once the trigger fires.</span></span><br/> |
| [<span data-ttu-id="5dc24-122">**StartBoundary**</span><span class="sxs-lookup"><span data-stu-id="5dc24-122">**StartBoundary**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="5dc24-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="5dc24-123">dateTime</span></span>                                                                 | <span data-ttu-id="5dc24-124">Data e ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="5dc24-124">The date and time when the trigger is activated.</span></span><br/>                                                            |



## <a name="attributes"></a><span data-ttu-id="5dc24-125">Attributi</span><span class="sxs-lookup"><span data-stu-id="5dc24-125">Attributes</span></span>



| <span data-ttu-id="5dc24-126">Nome</span><span class="sxs-lookup"><span data-stu-id="5dc24-126">Name</span></span> | <span data-ttu-id="5dc24-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dc24-127">Type</span></span> | <span data-ttu-id="5dc24-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc24-128">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="5dc24-129">id</span><span class="sxs-lookup"><span data-stu-id="5dc24-129">id</span></span>   | <span data-ttu-id="5dc24-130">ID</span><span class="sxs-lookup"><span data-stu-id="5dc24-130">ID</span></span>   | <span data-ttu-id="5dc24-131">Identificatore del trigger.</span><span class="sxs-lookup"><span data-stu-id="5dc24-131">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5dc24-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="5dc24-132">Remarks</span></span>

<span data-ttu-id="5dc24-133">I tipi complessi di trigger includono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="5dc24-133">Trigger complex types include the following.</span></span>

-   [<span data-ttu-id="5dc24-134">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-134">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-135">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-135">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-136">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-136">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-137">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-137">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-138">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-138">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-139">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-139">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md)
-   [<span data-ttu-id="5dc24-140">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="5dc24-140">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)

## <a name="requirements"></a><span data-ttu-id="5dc24-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dc24-141">Requirements</span></span>



| <span data-ttu-id="5dc24-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc24-142">Requirement</span></span> | <span data-ttu-id="5dc24-143">Valore</span><span class="sxs-lookup"><span data-stu-id="5dc24-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5dc24-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dc24-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc24-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dc24-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5dc24-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dc24-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc24-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5dc24-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5dc24-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dc24-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc24-149">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5dc24-149">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5dc24-150">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5dc24-150">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





