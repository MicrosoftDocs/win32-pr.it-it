---
title: Tipo complesso idleSettingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- Utilità di pianificazione di tipo complesso idleSettingsType
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301332"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="5bd68-104">Tipo complesso idleSettingsType</span><span class="sxs-lookup"><span data-stu-id="5bd68-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="5bd68-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5bd68-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
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
        <xs:element name="WaitTimeout"
            default="PT1H"
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5bd68-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5bd68-106">Child elements</span></span>



| <span data-ttu-id="5bd68-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5bd68-107">Element</span></span>                                                                                  | <span data-ttu-id="5bd68-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5bd68-108">Type</span></span>    | <span data-ttu-id="5bd68-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5bd68-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5bd68-110">**Duration**</span><span class="sxs-lookup"><span data-stu-id="5bd68-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="5bd68-111">Specifica la quantità di tempo consentita per l'avvio dell'attività in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="5bd68-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="5bd68-112">**RestartOnIdle**</span><span class="sxs-lookup"><span data-stu-id="5bd68-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="5bd68-113">boolean</span><span class="sxs-lookup"><span data-stu-id="5bd68-113">boolean</span></span> | <span data-ttu-id="5bd68-114">L'attività viene riavviata non appena viene avviata una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="5bd68-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="5bd68-115">**StopOnIdleEnd**</span><span class="sxs-lookup"><span data-stu-id="5bd68-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="5bd68-116">boolean</span><span class="sxs-lookup"><span data-stu-id="5bd68-116">boolean</span></span> | <span data-ttu-id="5bd68-117">Specifica che l'attività viene terminata se la condizione di inattività termina prima del superamento della durata di inattività.</span><span class="sxs-lookup"><span data-stu-id="5bd68-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="5bd68-118">**WaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="5bd68-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="5bd68-119">Specifica la quantità di tempo di attesa per l'avvio di una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="5bd68-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="5bd68-120">Se per questo elemento non viene specificato alcun valore, il servizio di Utilità di pianificazione attenderà per un periodo di tempo indefinito che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="5bd68-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5bd68-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bd68-121">Requirements</span></span>



| <span data-ttu-id="5bd68-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd68-122">Requirement</span></span> | <span data-ttu-id="5bd68-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5bd68-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bd68-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd68-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd68-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bd68-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5bd68-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd68-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd68-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bd68-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bd68-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bd68-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd68-129">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5bd68-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="5bd68-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5bd68-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





