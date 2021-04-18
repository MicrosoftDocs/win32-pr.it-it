---
title: Elemento Hidden (settingsType)
description: Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Utilità di pianificazione elemento nascosto
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef5ad479fe3107ed8fa79f0f86307254a9f33c4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302689"
---
# <a name="hidden-settingstype-element"></a><span data-ttu-id="e9f43-104">Elemento Hidden (settingsType)</span><span class="sxs-lookup"><span data-stu-id="e9f43-104">Hidden (settingsType) Element</span></span>

<span data-ttu-id="e9f43-105">Specifica che l'attività non sarà visibile nell'interfaccia utente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e9f43-105">Specifies that the task will not be visible in the UI by default.</span></span> <span data-ttu-id="e9f43-106">Tuttavia, gli amministratori possono eseguire l'override di questa impostazione tramite l'uso di un "Master switch" che rende visibili tutte le attività nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="e9f43-106">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="e9f43-107">L'elemento **Hidden** viene definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f43-107">The **Hidden** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e9f43-108">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="e9f43-108">Parent element</span></span>



| <span data-ttu-id="e9f43-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9f43-109">Element</span></span>                                                           | <span data-ttu-id="e9f43-110">Derivato da</span><span class="sxs-lookup"><span data-stu-id="e9f43-110">Derived from</span></span>                                                         | <span data-ttu-id="e9f43-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f43-111">Description</span></span>                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="e9f43-112">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="e9f43-112">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e9f43-113">**settingsType**</span><span class="sxs-lookup"><span data-stu-id="e9f43-113">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e9f43-114">Contiene le impostazioni utilizzate da Utilità di pianificazione per eseguire l'attività.</span><span class="sxs-lookup"><span data-stu-id="e9f43-114">Contains the settings that Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e9f43-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f43-115">Remarks</span></span>

<span data-ttu-id="e9f43-116">Per lo sviluppo in C++, vedere [**Proprietà Hidden di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span><span class="sxs-lookup"><span data-stu-id="e9f43-116">For C++ development, see [**Hidden Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden).</span></span>

<span data-ttu-id="e9f43-117">Per lo sviluppo di script, vedere [**TaskSettings. Hidden**](tasksettings-hidden.md).</span><span class="sxs-lookup"><span data-stu-id="e9f43-117">For script development, see [**TaskSettings.Hidden**](tasksettings-hidden.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f43-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f43-118">Requirements</span></span>



| <span data-ttu-id="e9f43-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f43-119">Requirement</span></span> | <span data-ttu-id="e9f43-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f43-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9f43-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f43-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f43-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9f43-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9f43-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f43-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f43-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9f43-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9f43-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f43-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f43-126">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e9f43-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





