---
title: Elemento period
description: Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Utilità di pianificazione elemento period
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479229"
---
# <a name="period-element"></a><span data-ttu-id="7491d-104">Elemento period</span><span class="sxs-lookup"><span data-stu-id="7491d-104">Period Element</span></span>

<span data-ttu-id="7491d-105">Specifica la frequenza con cui l'attività deve essere avviata durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="7491d-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="7491d-106">Il formato di questa stringa è *PnYnMnDTnHnMnS*, dove *NY* è il numero di anni, NM è il numero di mesi, *ND* è il numero di giorni, *T* è il separatore di data/ora, *NH* è il numero di ore, *nm* è il numero di minuti e *NS* è il numero di secondi (ad esempio, "PT5M" specifica 5 minuti e "P1M4DT2H5M" specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="7491d-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="7491d-107">Il valore minimo è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="7491d-107">The minimum value is one minute.</span></span> <span data-ttu-id="7491d-108">Per ulteriori informazioni sul tipo di durata, vedere [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="7491d-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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
```

<span data-ttu-id="7491d-109">L'elemento **period** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7491d-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="7491d-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="7491d-110">Parent element</span></span>



| <span data-ttu-id="7491d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="7491d-111">Element</span></span>                                                                                                                          | <span data-ttu-id="7491d-112">Derivato da</span><span class="sxs-lookup"><span data-stu-id="7491d-112">Derived from</span></span>                                                                               | <span data-ttu-id="7491d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7491d-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7491d-114">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="7491d-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="7491d-115">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="7491d-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="7491d-116">Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="7491d-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7491d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7491d-117">Remarks</span></span>

<span data-ttu-id="7491d-118">Per la programmazione in C++, questa impostazione inattiva viene specificata tramite la proprietà [**IMaintenanceSettings::P dere**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .</span><span class="sxs-lookup"><span data-stu-id="7491d-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="7491d-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="7491d-119">Examples</span></span>

<span data-ttu-id="7491d-120">Il codice XML seguente definisce l'attività di manutenzione con requisiti di periodicità impostati su 5 giorni.</span><span class="sxs-lookup"><span data-stu-id="7491d-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="7491d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7491d-121">Requirements</span></span>



| <span data-ttu-id="7491d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7491d-122">Requirement</span></span> | <span data-ttu-id="7491d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7491d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7491d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7491d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7491d-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7491d-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="7491d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7491d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7491d-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7491d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7491d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7491d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7491d-129">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7491d-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="7491d-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7491d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





