---
title: Elemento scadenza
description: Specifica quando l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione automatica.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Utilità di pianificazione elemento scadenza
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740831"
---
# <a name="deadline-element"></a><span data-ttu-id="e5866-104">Elemento scadenza</span><span class="sxs-lookup"><span data-stu-id="e5866-104">Deadline Element</span></span>

<span data-ttu-id="e5866-105">Specifica quando l'utilità di pianificazione deve avviare l'attività durante la manutenzione automatica di emergenza, se non è stata completata durante la normale manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="e5866-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="e5866-106">Il formato di questa stringa è *PnYnMnDTnHnMnS*, dove *NY* è il numero di anni, NM è il numero di mesi, *ND* è il numero di giorni, *T* è il separatore di data/ora, *NH* è il numero di ore, *nm* è il numero di minuti e *NS* è il numero di secondi (ad esempio, "PT5M" specifica 5 minuti e "P1M4DT2H5M" specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="e5866-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e5866-107">Il valore minimo è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="e5866-107">The minimum value is one minute.</span></span> <span data-ttu-id="e5866-108">Per ulteriori informazioni sul tipo di durata, vedere [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="e5866-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="e5866-109">La scadenza minima che un'attività può utilizzare è 1 giorno.</span><span class="sxs-lookup"><span data-stu-id="e5866-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="e5866-110">Il valore dell'elemento **scadenza** deve essere maggiore del valore dell'elemento [**period**](taskschedulerschema-period-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e5866-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="e5866-111">Se non viene specificata la scadenza, l'attività non verrà avviata durante la manutenzione automatica di emergenza.</span><span class="sxs-lookup"><span data-stu-id="e5866-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
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

<span data-ttu-id="e5866-112">L'elemento **scadenza** è definito dal tipo complesso [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e5866-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e5866-113">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e5866-113">Parent element</span></span>



| <span data-ttu-id="e5866-114">Elemento</span><span class="sxs-lookup"><span data-stu-id="e5866-114">Element</span></span>                                                                                                                          | <span data-ttu-id="e5866-115">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e5866-115">Derived from</span></span>                                                                               | <span data-ttu-id="e5866-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5866-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5866-117">**MaintenanceSettings (maintenanceSettingsType)**</span><span class="sxs-lookup"><span data-stu-id="e5866-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="e5866-118">**maintenanceSettingsType**</span><span class="sxs-lookup"><span data-stu-id="e5866-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="e5866-119">Specifica le impostazioni dell'attività che l'utilità di pianificazione utilizzerà per avviare l'attività durante la manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="e5866-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e5866-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5866-120">Remarks</span></span>

<span data-ttu-id="e5866-121">Per la programmazione in C++, questa impostazione inattiva viene specificata tramite la proprietà [**IMaintenanceSettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .</span><span class="sxs-lookup"><span data-stu-id="e5866-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="e5866-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="e5866-122">Examples</span></span>

<span data-ttu-id="e5866-123">Il codice XML seguente definisce un calendario dei mesi che esegue l'attività a marzo.</span><span class="sxs-lookup"><span data-stu-id="e5866-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="e5866-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5866-124">Requirements</span></span>



| <span data-ttu-id="e5866-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5866-125">Requirement</span></span> | <span data-ttu-id="e5866-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e5866-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e5866-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5866-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e5866-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e5866-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="e5866-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5866-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e5866-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e5866-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5866-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5866-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5866-132">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e5866-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="e5866-133">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e5866-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





