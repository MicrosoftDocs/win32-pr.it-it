---
title: Elemento WaitTimeout (idleSettingsType)
description: Specifica la quantità di tempo per cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Utilità di pianificazione elemento WaitTimeout
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518478"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="3e889-104">Elemento WaitTimeout (idleSettingsType)</span><span class="sxs-lookup"><span data-stu-id="3e889-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="3e889-105">Specifica la quantità di tempo per cui il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="3e889-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="3e889-106">Se per questo elemento non viene specificato alcun valore, il servizio di Utilità di pianificazione attenderà per un periodo di tempo indefinito che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="3e889-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="3e889-107">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="3e889-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="3e889-108">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="3e889-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="3e889-109">Il tempo minimo consentito è pari a 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="3e889-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
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
```

<span data-ttu-id="3e889-110">L'elemento è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3e889-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="3e889-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="3e889-111">Parent element</span></span>



| <span data-ttu-id="3e889-112">Elemento</span><span class="sxs-lookup"><span data-stu-id="3e889-112">Element</span></span>                                                                       | <span data-ttu-id="3e889-113">Derivato da</span><span class="sxs-lookup"><span data-stu-id="3e889-113">Derived from</span></span>                                                                 | <span data-ttu-id="3e889-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e889-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e889-115">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="3e889-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="3e889-116">**idleSettingsType**</span><span class="sxs-lookup"><span data-stu-id="3e889-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="3e889-117">Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="3e889-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3e889-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e889-118">Remarks</span></span>

<span data-ttu-id="3e889-119">Per lo sviluppo di script, questa impostazione di inattività viene specificata tramite la proprietà [**IdleSettings. WaitTimeout**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="3e889-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="3e889-120">Per lo sviluppo in C++, questa impostazione di inattività viene specificata tramite la proprietà [**IIdleSettings:: WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .</span><span class="sxs-lookup"><span data-stu-id="3e889-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="3e889-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e889-121">Examples</span></span>

<span data-ttu-id="3e889-122">Il codice XML seguente definisce un'impostazione di inattività che attende 24 ore affinché si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="3e889-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="3e889-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e889-123">Requirements</span></span>



| <span data-ttu-id="3e889-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e889-124">Requirement</span></span> | <span data-ttu-id="3e889-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3e889-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e889-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e889-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e889-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e889-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3e889-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e889-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e889-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e889-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e889-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e889-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e889-131">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3e889-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3e889-132">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3e889-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





