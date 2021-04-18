---
title: Tipo complesso timeTriggerType
description: Definisce il tipo di base per l'elemento TimeTrigger.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- Utilità di pianificazione di tipo complesso timeTriggerType
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301146"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="04326-104">Tipo complesso timeTriggerType</span><span class="sxs-lookup"><span data-stu-id="04326-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="04326-105">Definisce il tipo di base per l'elemento [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04326-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="04326-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="04326-106">Child elements</span></span>



| <span data-ttu-id="04326-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="04326-107">Element</span></span>                                                                        | <span data-ttu-id="04326-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="04326-108">Type</span></span>     | <span data-ttu-id="04326-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04326-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04326-110">**RandomDelay**</span><span class="sxs-lookup"><span data-stu-id="04326-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="04326-111">duration</span><span class="sxs-lookup"><span data-stu-id="04326-111">duration</span></span> | <span data-ttu-id="04326-112">Specifica il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger.</span><span class="sxs-lookup"><span data-stu-id="04326-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="04326-113">Il formato di questa stringa è P <days> DT <hours> H <minutes> M <seconds> S (ad esempio, P2DT5S è un ritardo di 2 giorni e 5 secondi).</span><span class="sxs-lookup"><span data-stu-id="04326-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="04326-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="04326-114">Remarks</span></span>

<span data-ttu-id="04326-115">Si noti che questo elemento non aggiunge elementi figlio a quelli definiti dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="04326-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="04326-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04326-116">Requirements</span></span>



| <span data-ttu-id="04326-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04326-117">Requirement</span></span> | <span data-ttu-id="04326-118">Valore</span><span class="sxs-lookup"><span data-stu-id="04326-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="04326-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04326-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04326-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04326-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="04326-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04326-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04326-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04326-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="04326-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04326-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04326-124">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="04326-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="04326-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="04326-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





