---
title: Tipo complesso repetitionType
description: Definisce gli elementi figlio e le informazioni sulla sequenza per l'elemento di ripetizione (triggerBaseType).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- Utilità di pianificazione di tipo complesso repetitionType
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400793"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="3e561-104">Tipo complesso repetitionType</span><span class="sxs-lookup"><span data-stu-id="3e561-104">repetitionType Complex Type</span></span>

<span data-ttu-id="3e561-105">Definisce gli elementi figlio e le informazioni sulla sequenza per l'elemento di [**ripetizione (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3e561-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3e561-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3e561-106">Child elements</span></span>



| <span data-ttu-id="3e561-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3e561-107">Element</span></span>                                                                                   | <span data-ttu-id="3e561-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e561-108">Type</span></span>    | <span data-ttu-id="3e561-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e561-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e561-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="3e561-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="3e561-111">Specifica il tempo di ripetizione del pattern.</span><span class="sxs-lookup"><span data-stu-id="3e561-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="3e561-112">Se non viene specificato alcun valore, il modello viene ripetuto per un periodo illimitato.</span><span class="sxs-lookup"><span data-stu-id="3e561-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="3e561-113">**Interval**</span><span class="sxs-lookup"><span data-stu-id="3e561-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="3e561-114">Specifica la quantità di tempo tra ogni riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="3e561-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="3e561-115">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="3e561-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="3e561-116">boolean</span><span class="sxs-lookup"><span data-stu-id="3e561-116">boolean</span></span> | <span data-ttu-id="3e561-117">Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="3e561-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="3e561-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e561-118">Requirements</span></span>



| <span data-ttu-id="3e561-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e561-119">Requirement</span></span> | <span data-ttu-id="3e561-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3e561-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e561-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e561-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e561-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e561-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3e561-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e561-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e561-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e561-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e561-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e561-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e561-126">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3e561-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3e561-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3e561-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





