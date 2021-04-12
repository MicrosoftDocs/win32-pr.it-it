---
title: Tipo complesso bootTriggerType
description: Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento BootTrigger.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- Utilità di pianificazione di tipo complesso bootTriggerType
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478191"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="aa65c-104">Tipo complesso bootTriggerType</span><span class="sxs-lookup"><span data-stu-id="aa65c-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="aa65c-105">Definisce l'elemento figlio e le informazioni di sequenziazione per l'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aa65c-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="aa65c-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="aa65c-106">Child elements</span></span>



| <span data-ttu-id="aa65c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa65c-107">Element</span></span>                                                            | <span data-ttu-id="aa65c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa65c-108">Type</span></span>     | <span data-ttu-id="aa65c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa65c-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa65c-110">**Ritardo**</span><span class="sxs-lookup"><span data-stu-id="aa65c-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="aa65c-111">duration</span><span class="sxs-lookup"><span data-stu-id="aa65c-111">duration</span></span> | <span data-ttu-id="aa65c-112">Intervallo di tempo tra il momento in cui il sistema viene avviato e il momento in cui viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="aa65c-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="aa65c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa65c-113">Remarks</span></span>

<span data-ttu-id="aa65c-114">Oltre all'elemento figlio definito qui, l'elemento [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) usa anche elementi figlio definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="aa65c-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa65c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa65c-115">Requirements</span></span>



| <span data-ttu-id="aa65c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa65c-116">Requirement</span></span> | <span data-ttu-id="aa65c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="aa65c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa65c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa65c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa65c-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa65c-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa65c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa65c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa65c-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa65c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa65c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa65c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa65c-123">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="aa65c-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="aa65c-124">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="aa65c-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





