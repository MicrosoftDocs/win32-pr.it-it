---
title: Elemento DeleteExpiredTaskAfter (settingsType)
description: Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Utilità di pianificazione elemento DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301338"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="d3970-104">Elemento DeleteExpiredTaskAfter (settingsType)</span><span class="sxs-lookup"><span data-stu-id="d3970-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="d3970-105">Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.</span><span class="sxs-lookup"><span data-stu-id="d3970-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="d3970-106">Se per questo elemento non viene specificato alcun valore, il servizio Utilità di pianificazione non eliminerà l'attività.</span><span class="sxs-lookup"><span data-stu-id="d3970-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="d3970-107">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="d3970-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="d3970-108">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="d3970-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="d3970-109">L'elemento **DeleteExpiredTaskAfter** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d3970-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d3970-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="d3970-110">Parent element</span></span>



| <span data-ttu-id="d3970-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="d3970-111">Element</span></span>                                                           | <span data-ttu-id="d3970-112">Derivato da</span><span class="sxs-lookup"><span data-stu-id="d3970-112">Derived from</span></span>                                                         | <span data-ttu-id="d3970-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3970-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3970-114">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="d3970-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="d3970-115">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="d3970-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="d3970-116">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="d3970-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d3970-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3970-117">Remarks</span></span>

<span data-ttu-id="d3970-118">Per lo sviluppo in C++, vedere [**la proprietà DeleteExpiredTaskAfter di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="d3970-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="d3970-119">Per lo sviluppo di script, vedere [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="d3970-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d3970-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3970-120">Examples</span></span>

<span data-ttu-id="d3970-121">Nel codice XML seguente viene definito un elemento Settings che elimina un'attività scaduta dopo una settimana.</span><span class="sxs-lookup"><span data-stu-id="d3970-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="d3970-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3970-122">Requirements</span></span>



| <span data-ttu-id="d3970-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3970-123">Requirement</span></span> | <span data-ttu-id="d3970-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d3970-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3970-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3970-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3970-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3970-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d3970-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3970-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3970-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3970-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3970-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3970-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3970-130">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d3970-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





