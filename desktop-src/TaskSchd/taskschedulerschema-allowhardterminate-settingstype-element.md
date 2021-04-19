---
title: Elemento AllowHardTerminate (settingsType)
description: Specifica che l'attività può essere terminata utilizzando TerminateProcess.
ms.assetid: 093a3cc6-d3e1-48e3-bc9e-0b15df2a54de
keywords:
- Elemento AllowHardTerminate (settingsType) Utilità di pianificazione
- Utilità di pianificazione elemento AllowHardTerminate
topic_type:
- apiref
api_name:
- AllowHardTerminate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eba987b42206121b91b3c096f298eac32cf52b38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301240"
---
# <a name="allowhardterminate-settingstype-element"></a><span data-ttu-id="1c991-105">Elemento AllowHardTerminate (settingsType)</span><span class="sxs-lookup"><span data-stu-id="1c991-105">AllowHardTerminate (settingsType) Element</span></span>

<span data-ttu-id="1c991-106">Specifica che l'attività può essere terminata utilizzando TerminateProcess.</span><span class="sxs-lookup"><span data-stu-id="1c991-106">Specifies that the task may be terminated using TerminateProcess.</span></span>

``` syntax
<xs:element name="AllowHardTerminate"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

<span data-ttu-id="1c991-107">L'elemento **AllowHardTerminate** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1c991-107">The **AllowHardTerminate** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1c991-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="1c991-108">Parent element</span></span>



| <span data-ttu-id="1c991-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1c991-109">Element</span></span>                                                           | <span data-ttu-id="1c991-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="1c991-110">Derived from</span></span>                                                 | <span data-ttu-id="1c991-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c991-111">Description</span></span>                                                                        |
|-------------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c991-112">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="1c991-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="1c991-113">**taskType**</span><span class="sxs-lookup"><span data-stu-id="1c991-113">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="1c991-114">Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="1c991-114">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1c991-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c991-115">Remarks</span></span>

<span data-ttu-id="1c991-116">Per lo sviluppo in C++, vedere la [**Proprietà AllowHardTerminate di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span><span class="sxs-lookup"><span data-stu-id="1c991-116">For C++ development, see the [**AllowHardTerminate property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowhardterminate).</span></span>

<span data-ttu-id="1c991-117">Per lo sviluppo di script, vedere [**TaskSettings. AllowHardTerminate**](tasksettings-allowhardterminate.md).</span><span class="sxs-lookup"><span data-stu-id="1c991-117">For script development, see [**TaskSettings.AllowHardTerminate**](tasksettings-allowhardterminate.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1c991-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="1c991-118">Examples</span></span>

<span data-ttu-id="1c991-119">Per un esempio completo del codice XML per un'attività che consente la terminazione rigida, vedere l' [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1c991-119">For a complete example of the XML for a task that allows hard termination, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c991-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c991-120">Requirements</span></span>



| <span data-ttu-id="1c991-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c991-121">Requirement</span></span> | <span data-ttu-id="1c991-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1c991-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c991-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c991-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c991-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c991-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c991-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c991-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c991-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c991-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c991-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c991-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c991-128">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="1c991-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





