---
title: Oggetto NetworkSettings
description: Per gli script, fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Utilità di pianificazione oggetto NetworkSettings
- Oggetto NetworkSettings Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477201"
---
# <a name="networksettings-object"></a><span data-ttu-id="0e3d6-105">Oggetto NetworkSettings</span><span class="sxs-lookup"><span data-stu-id="0e3d6-105">NetworkSettings object</span></span>

<span data-ttu-id="0e3d6-106">Per gli script, fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="0e3d6-107">Membri</span><span class="sxs-lookup"><span data-stu-id="0e3d6-107">Members</span></span>

<span data-ttu-id="0e3d6-108">L'oggetto **NetworkSettings** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0e3d6-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="0e3d6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e3d6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e3d6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e3d6-110">Properties</span></span>

<span data-ttu-id="0e3d6-111">L'oggetto **NetworkSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="0e3d6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0e3d6-112">Property</span></span>                                        | <span data-ttu-id="0e3d6-113">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0e3d6-113">Access type</span></span>           | <span data-ttu-id="0e3d6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e3d6-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e3d6-115">**ID**</span><span class="sxs-lookup"><span data-stu-id="0e3d6-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="0e3d6-116">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0e3d6-116">Read/write</span></span><br/> | <span data-ttu-id="0e3d6-117">Ottiene o imposta un valore GUID che identifica un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="0e3d6-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0e3d6-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="0e3d6-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0e3d6-119">Read/write</span></span><br/> | <span data-ttu-id="0e3d6-120">Ottiene o imposta il nome di un profilo di rete.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="0e3d6-121">Il nome viene usato a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e3d6-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e3d6-122">Remarks</span></span>

<span data-ttu-id="0e3d6-123">Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, le impostazioni di rete vengono specificate usando l'elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0e3d6-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3d6-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e3d6-124">Requirements</span></span>



| <span data-ttu-id="0e3d6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3d6-125">Requirement</span></span> | <span data-ttu-id="0e3d6-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0e3d6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3d6-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e3d6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3d6-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e3d6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e3d6-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e3d6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3d6-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e3d6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e3d6-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e3d6-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e3d6-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e3d6-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e3d6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3d6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e3d6-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3d6-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e3d6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e3d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3d6-136">Oggetti Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0e3d6-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="0e3d6-137">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="0e3d6-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





