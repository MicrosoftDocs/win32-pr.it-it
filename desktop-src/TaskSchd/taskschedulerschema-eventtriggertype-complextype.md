---
title: Tipo complesso eventTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento EventTrigger.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Utilità di pianificazione di tipo complesso eventTriggerType
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302168"
---
# <a name="eventtriggertype-complex-type"></a><span data-ttu-id="6752e-104">Tipo complesso eventTriggerType</span><span class="sxs-lookup"><span data-stu-id="6752e-104">eventTriggerType Complex Type</span></span>

<span data-ttu-id="6752e-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6752e-105">Defines the child elements and sequencing information for the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6752e-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6752e-106">Child elements</span></span>



| <span data-ttu-id="6752e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="6752e-107">Element</span></span>                                                                           | <span data-ttu-id="6752e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6752e-108">Type</span></span>                                                                    | <span data-ttu-id="6752e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6752e-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6752e-110">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="6752e-110">**Delay**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="6752e-111">duration</span><span class="sxs-lookup"><span data-stu-id="6752e-111">duration</span></span>                                                                | <span data-ttu-id="6752e-112">Specifica la quantità di tempo tra il momento in cui si verifica l'evento e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6752e-112">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="6752e-113">**Abbonamento**</span><span class="sxs-lookup"><span data-stu-id="6752e-113">**Subscription**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | [<span data-ttu-id="6752e-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="6752e-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="6752e-115">Specifica la query XPath che identifica l'evento che attiva il trigger.</span><span class="sxs-lookup"><span data-stu-id="6752e-115">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="6752e-116">**ValueQueries**</span><span class="sxs-lookup"><span data-stu-id="6752e-116">**ValueQueries**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="6752e-117">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="6752e-117">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md)      | <span data-ttu-id="6752e-118">Specifica una sequenza di elementi ognuno dei quali contiene un nome e un valore di query XPath.</span><span class="sxs-lookup"><span data-stu-id="6752e-118">Specifies a sequence of elements that each contain a name and an XPath query value.</span></span> <span data-ttu-id="6752e-119">Le query vengono applicate a un evento restituito dalla sottoscrizione dell'evento specificato nell'elemento [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6752e-119">The queries are applied to an event returned from the event subscription specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="6752e-120">Il nome del valore della query XPath può essere utilizzato come variabile nell'elemento [**Body**](taskschedulerschema-body-showmessagetype-element.md) nella sezione dell'azione [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) di un'attività.</span><span class="sxs-lookup"><span data-stu-id="6752e-120">The name for the XPath query value can be used as a variable in the [**Body**](taskschedulerschema-body-showmessagetype-element.md) element in the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) action section of a task.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="6752e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6752e-121">Remarks</span></span>

<span data-ttu-id="6752e-122">Oltre all'elemento figlio definito qui, l'elemento [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6752e-122">In addition to the child element defined here, the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6752e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6752e-123">Requirements</span></span>



| <span data-ttu-id="6752e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6752e-124">Requirement</span></span> | <span data-ttu-id="6752e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6752e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6752e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6752e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6752e-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6752e-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6752e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6752e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6752e-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6752e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6752e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6752e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6752e-131">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6752e-131">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="6752e-132">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="6752e-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





