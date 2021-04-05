---
title: Interfaccia IRDVTaskPluginNotifySink
description: L'interfaccia IRDVTaskPluginNotifySink viene utilizzata dall'agente attività per comunicare con l'agente di trigger.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742071"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="e3060-105">Interfaccia IRDVTaskPluginNotifySink</span><span class="sxs-lookup"><span data-stu-id="e3060-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="e3060-106">L'interfaccia **IRDVTaskPluginNotifySink** viene utilizzata dall'agente attività per comunicare con l'agente di trigger.</span><span class="sxs-lookup"><span data-stu-id="e3060-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="e3060-107">Un puntatore a questa interfaccia viene passato all'agente attività nel metodo [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="e3060-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="e3060-108">Membri</span><span class="sxs-lookup"><span data-stu-id="e3060-108">Members</span></span>

<span data-ttu-id="e3060-109">L'interfaccia **IRDVTaskPluginNotifySink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e3060-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e3060-110">**IRDVTaskPluginNotifySink** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3060-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="e3060-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e3060-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e3060-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e3060-112">Methods</span></span>

<span data-ttu-id="e3060-113">L'interfaccia **IRDVTaskPluginNotifySink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e3060-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="e3060-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="e3060-114">Method</span></span>                                                                  | <span data-ttu-id="e3060-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3060-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="e3060-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="e3060-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="e3060-117">Chiamato dall'agente attività per eliminare un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="e3060-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="e3060-118">**OnTaskStateChange**</span><span class="sxs-lookup"><span data-stu-id="e3060-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="e3060-119">Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e3060-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="e3060-120">**Con terminazione**</span><span class="sxs-lookup"><span data-stu-id="e3060-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="e3060-121">Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="e3060-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="e3060-122">**ScheduleTask**</span><span class="sxs-lookup"><span data-stu-id="e3060-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="e3060-123">Chiamato dall'agente attività per pianificare un'attività.</span><span class="sxs-lookup"><span data-stu-id="e3060-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="e3060-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3060-124">Remarks</span></span>

<span data-ttu-id="e3060-125">Sebbene questa interfaccia sia supportata nei sistemi operativi indicati nei requisiti indicati di seguito, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="e3060-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3060-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3060-126">Requirements</span></span>



| <span data-ttu-id="e3060-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3060-127">Requirement</span></span> | <span data-ttu-id="e3060-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e3060-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="e3060-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3060-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e3060-130">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="e3060-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="e3060-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3060-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e3060-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e3060-132">Windows Server 2008 R2</span></span><br/> |



 

