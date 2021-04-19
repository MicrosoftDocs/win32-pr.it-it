---
title: Tipo complesso logonTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento LogonTrigger.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Utilità di pianificazione di tipo complesso logonTriggerType
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302688"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="c36b0-104">Tipo complesso logonTriggerType</span><span class="sxs-lookup"><span data-stu-id="c36b0-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="c36b0-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c36b0-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c36b0-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c36b0-106">Child elements</span></span>



| <span data-ttu-id="c36b0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="c36b0-107">Element</span></span>                                                               | <span data-ttu-id="c36b0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c36b0-108">Type</span></span>                                                                    | <span data-ttu-id="c36b0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c36b0-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c36b0-110">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="c36b0-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="c36b0-111">duration</span><span class="sxs-lookup"><span data-stu-id="c36b0-111">duration</span></span>                                                                | <span data-ttu-id="c36b0-112">Intervallo di tempo tra il momento in cui l'utente esegue l'accesso e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="c36b0-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="c36b0-113">**UserId**</span><span class="sxs-lookup"><span data-stu-id="c36b0-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="c36b0-114">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="c36b0-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="c36b0-115">Identificatore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c36b0-115">Identifier of the user.</span></span> <span data-ttu-id="c36b0-116">L'attività viene avviata quando l'utente accede al computer.</span><span class="sxs-lookup"><span data-stu-id="c36b0-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c36b0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c36b0-117">Remarks</span></span>

<span data-ttu-id="c36b0-118">Oltre agli elementi figlio definiti in questa sezione, l'elemento [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c36b0-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36b0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c36b0-119">Requirements</span></span>



| <span data-ttu-id="c36b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c36b0-120">Requirement</span></span> | <span data-ttu-id="c36b0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c36b0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c36b0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c36b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c36b0-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c36b0-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c36b0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c36b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c36b0-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c36b0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c36b0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c36b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36b0-127">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c36b0-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="c36b0-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="c36b0-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





