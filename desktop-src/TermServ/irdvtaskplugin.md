---
title: Interfaccia IRDVTaskPlugin
description: L'interfaccia IRDVTaskPlugin viene implementata da un agente attività aggiornamento macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti del sistema per una macchina virtuale.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto
- Interfaccia IRDVTaskPlugin Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964905"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="ca238-105">Interfaccia IRDVTaskPlugin</span><span class="sxs-lookup"><span data-stu-id="ca238-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="ca238-106">L'interfaccia **IRDVTaskPlugin** viene implementata da un *agente attività* aggiornamento macchina virtuale per consentire all'agente attività di gestire gli aggiornamenti del sistema per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca238-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="ca238-107">Questa interfaccia viene utilizzata dall' *agente trigger*, che viene implementato dal sistema host.</span><span class="sxs-lookup"><span data-stu-id="ca238-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="ca238-108">Membri</span><span class="sxs-lookup"><span data-stu-id="ca238-108">Members</span></span>

<span data-ttu-id="ca238-109">L'interfaccia **IRDVTaskPlugin** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ca238-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ca238-110">**IRDVTaskPlugin** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ca238-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="ca238-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ca238-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ca238-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca238-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ca238-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ca238-113">Methods</span></span>

<span data-ttu-id="ca238-114">L'interfaccia **IRDVTaskPlugin** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ca238-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="ca238-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ca238-115">Method</span></span>                                          | <span data-ttu-id="ca238-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca238-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="ca238-117">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="ca238-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="ca238-118">Chiamato per inizializzare l'agente attività.</span><span class="sxs-lookup"><span data-stu-id="ca238-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="ca238-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="ca238-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="ca238-120">Chiamato per avviare l'attività di aggiornamento nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ca238-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="ca238-121">**Terminare**</span><span class="sxs-lookup"><span data-stu-id="ca238-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="ca238-122">Chiamato quando l'agente attività viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="ca238-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="ca238-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca238-123">Properties</span></span>

<span data-ttu-id="ca238-124">L'interfaccia **IRDVTaskPlugin** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca238-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="ca238-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ca238-125">Property</span></span>                                                   | <span data-ttu-id="ca238-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ca238-126">Access type</span></span>          | <span data-ttu-id="ca238-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca238-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="ca238-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="ca238-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="ca238-129">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ca238-129">Read-only</span></span><br/> | <span data-ttu-id="ca238-130">Contiene il nome visualizzato dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="ca238-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca238-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca238-131">Remarks</span></span>

<span data-ttu-id="ca238-132">L'agente attività viene eseguito nella macchina virtuale quando la macchina virtuale è pianificata per un aggiornamento del sistema.</span><span class="sxs-lookup"><span data-stu-id="ca238-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="ca238-133">L'agente attività Aggiorna la macchina virtuale quando viene chiamato il metodo [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="ca238-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="ca238-134">Per registrare l'agente attività, aggiungere la chiave seguente al registro di sistema della macchina virtuale:</span><span class="sxs-lookup"><span data-stu-id="ca238-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="ca238-135">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\ **plugin** attività \\ **TaskAgentName**</span><span class="sxs-lookup"><span data-stu-id="ca238-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="ca238-136">In questa chiave del registro di sistema aggiungere i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca238-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="ca238-137">Nome</span><span class="sxs-lookup"><span data-stu-id="ca238-137">Name</span></span>                     | <span data-ttu-id="ca238-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca238-138">Type</span></span>                      | <span data-ttu-id="ca238-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca238-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ca238-140">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="ca238-140">**CLSID**</span></span><br/>     | <span data-ttu-id="ca238-141">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="ca238-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="ca238-142">Stringa che rappresenta il **CLSID** dell'agente attività.</span><span class="sxs-lookup"><span data-stu-id="ca238-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="ca238-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ca238-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="ca238-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ca238-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="ca238-145">0 se l'agente attività è disabilitato o 1 se l'agente attività è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ca238-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="ca238-146">È possibile registrare più di un agente attività, ma verrà usato un solo agente attività.</span><span class="sxs-lookup"><span data-stu-id="ca238-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="ca238-147">Se è abilitato più di un agente attività, verrà utilizzato solo il primo oggetto trovato.</span><span class="sxs-lookup"><span data-stu-id="ca238-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="ca238-148">Sebbene questa interfaccia sia supportata nei sistemi operativi indicati nei requisiti indicati di seguito, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ca238-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca238-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca238-149">Requirements</span></span>



| <span data-ttu-id="ca238-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca238-150">Requirement</span></span> | <span data-ttu-id="ca238-151">Valore</span><span class="sxs-lookup"><span data-stu-id="ca238-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="ca238-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca238-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ca238-153">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ca238-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="ca238-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca238-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ca238-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca238-155">Windows Server 2008 R2</span></span><br/> |



 

