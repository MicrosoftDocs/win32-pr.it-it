---
title: Tipo complesso maintenanceSettingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- Utilità di pianificazione di tipo complesso maintenanceSettingsType
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742762"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="3db92-104">Tipo complesso maintenanceSettingsType</span><span class="sxs-lookup"><span data-stu-id="3db92-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="3db92-105">Definisce gli elementi figlio e le informazioni di sequenziazione per l'elemento [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3db92-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3db92-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="3db92-106">Child elements</span></span>



| <span data-ttu-id="3db92-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3db92-107">Element</span></span>                                                                        | <span data-ttu-id="3db92-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3db92-108">Type</span></span>    | <span data-ttu-id="3db92-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3db92-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3db92-110">**Scadenza**</span><span class="sxs-lookup"><span data-stu-id="3db92-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="3db92-111">Specifica il periodo di tempo dopo il quale l'utilità di pianificazione tenterà di avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione.</span><span class="sxs-lookup"><span data-stu-id="3db92-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="3db92-112">**Exclusive**</span><span class="sxs-lookup"><span data-stu-id="3db92-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="3db92-113">boolean</span><span class="sxs-lookup"><span data-stu-id="3db92-113">boolean</span></span> | <span data-ttu-id="3db92-114">Se è impostato su true, l'attività verrà avviata esclusivamente tra le altre attività di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="3db92-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="3db92-115">**Periodo**</span><span class="sxs-lookup"><span data-stu-id="3db92-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="3db92-116">Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="3db92-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="3db92-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3db92-117">Requirements</span></span>



| <span data-ttu-id="3db92-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3db92-118">Requirement</span></span> | <span data-ttu-id="3db92-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3db92-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3db92-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3db92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3db92-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3db92-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="3db92-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3db92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3db92-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3db92-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3db92-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3db92-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db92-125">Tipi complessi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3db92-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3db92-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3db92-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





