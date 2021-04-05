---
title: Elemento ExecutionTimeLimit (settingsType)
description: Quantità di tempo consentita per completare l'attività.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Utilità di pianificazione elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873457"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="1853f-104">Elemento ExecutionTimeLimit (settingsType)</span><span class="sxs-lookup"><span data-stu-id="1853f-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="1853f-105">Quantità di tempo consentita per completare l'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="1853f-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="1853f-106">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="1853f-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="1853f-107">Il valore PT0S consentirà l'esecuzione illimitata dell'attività.</span><span class="sxs-lookup"><span data-stu-id="1853f-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="1853f-108">L'elemento **ExecutionTimeLimit** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1853f-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1853f-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1853f-109">Parent element</span></span>



| <span data-ttu-id="1853f-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="1853f-110">Element</span></span>                                                           | <span data-ttu-id="1853f-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1853f-111">Derived from</span></span>                                                         | <span data-ttu-id="1853f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1853f-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1853f-113">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="1853f-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1853f-114">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="1853f-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="1853f-115">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="1853f-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1853f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1853f-116">Remarks</span></span>

<span data-ttu-id="1853f-117">Per lo sviluppo in C++, vedere [**la proprietà ExecutionTimeLimit di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="1853f-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="1853f-118">Per lo sviluppo di script, vedere [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="1853f-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1853f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1853f-119">Requirements</span></span>



| <span data-ttu-id="1853f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1853f-120">Requirement</span></span> | <span data-ttu-id="1853f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1853f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1853f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1853f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1853f-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1853f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1853f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1853f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1853f-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1853f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1853f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1853f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1853f-127">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1853f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





