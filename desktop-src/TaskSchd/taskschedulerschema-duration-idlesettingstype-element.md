---
title: Duration (idleSettingsType)-elemento
description: Specifica per quanto tempo il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Utilità di pianificazione elemento Duration
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517565"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="2c852-104">Duration (idleSettingsType)-elemento</span><span class="sxs-lookup"><span data-stu-id="2c852-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="2c852-105">Specifica per quanto tempo il computer deve trovarsi in uno stato di inattività prima dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2c852-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="2c852-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="2c852-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="2c852-107">Il valore minimo è di un minuto.</span><span class="sxs-lookup"><span data-stu-id="2c852-107">The minimum value is one minute.</span></span> <span data-ttu-id="2c852-108">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="2c852-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
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
```

<span data-ttu-id="2c852-109">L'elemento è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c852-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2c852-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="2c852-110">Parent element</span></span>



| <span data-ttu-id="2c852-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="2c852-111">Element</span></span>                                                                       | <span data-ttu-id="2c852-112">Derivato da</span><span class="sxs-lookup"><span data-stu-id="2c852-112">Derived from</span></span>                                                                 | <span data-ttu-id="2c852-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c852-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c852-114">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="2c852-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="2c852-115">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="2c852-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="2c852-116">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="2c852-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c852-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c852-117">Remarks</span></span>

<span data-ttu-id="2c852-118">Per la programmazione di script, questa impostazione di inattività viene specificata tramite la proprietà [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) .</span><span class="sxs-lookup"><span data-stu-id="2c852-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="2c852-119">Per la programmazione in C++, questa impostazione di inattività viene specificata tramite la proprietà [**IIdleSettings:: IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .</span><span class="sxs-lookup"><span data-stu-id="2c852-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="2c852-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="2c852-120">Examples</span></span>

<span data-ttu-id="2c852-121">Il codice XML seguente definisce un'impostazione inattiva che consente 5 minuti per l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2c852-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="2c852-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c852-122">Requirements</span></span>



| <span data-ttu-id="2c852-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c852-123">Requirement</span></span> | <span data-ttu-id="2c852-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2c852-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c852-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c852-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2c852-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c852-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c852-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c852-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2c852-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c852-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c852-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c852-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c852-130">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2c852-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2c852-131">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="2c852-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





