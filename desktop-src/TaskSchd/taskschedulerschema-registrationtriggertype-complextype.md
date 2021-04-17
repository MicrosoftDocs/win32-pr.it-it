---
title: Tipo complesso registrationTriggerType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento RegistrationTrigger.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- Utilità di pianificazione di tipo complesso registrationTriggerType
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400794"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="59950-104">Tipo complesso registrationTriggerType</span><span class="sxs-lookup"><span data-stu-id="59950-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="59950-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="59950-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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

## <a name="child-elements"></a><span data-ttu-id="59950-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="59950-106">Child elements</span></span>



| <span data-ttu-id="59950-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="59950-107">Element</span></span>                                                                    | <span data-ttu-id="59950-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="59950-108">Type</span></span>     | <span data-ttu-id="59950-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59950-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59950-110">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="59950-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="59950-111">duration</span><span class="sxs-lookup"><span data-stu-id="59950-111">duration</span></span> | <span data-ttu-id="59950-112">Specifica l'intervallo di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="59950-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="59950-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="59950-113">Remarks</span></span>

<span data-ttu-id="59950-114">Oltre agli elementi figlio definiti in questa sezione, l'elemento [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="59950-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="59950-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59950-115">Requirements</span></span>



| <span data-ttu-id="59950-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59950-116">Requirement</span></span> | <span data-ttu-id="59950-117">Valore</span><span class="sxs-lookup"><span data-stu-id="59950-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59950-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59950-118">Minimum supported client</span></span><br/> | <span data-ttu-id="59950-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59950-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59950-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59950-120">Minimum supported server</span></span><br/> | <span data-ttu-id="59950-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59950-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59950-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59950-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59950-123">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="59950-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="59950-124">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="59950-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





