---
description: Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll autoregistrate usando le azioni SelfRegModules e SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Specifica dell'ordine di registrazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485380"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="85944-103">Specifica dell'ordine di registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="85944-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="85944-104">Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione delle dll autoregistrate usando le azioni [SelfRegModules](selfregmodules-action.md) e [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="85944-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="85944-105">Queste azioni registrano tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="85944-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="85944-106">Il programma di installazione non registra autonomamente i file exe.</span><span class="sxs-lookup"><span data-stu-id="85944-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="85944-107">Per specificare l'ordine in cui il programma di installazione registra o Annulla la registrazione dei moduli, è necessario usare due [azioni personalizzate](custom-actions.md) per ogni modulo.</span><span class="sxs-lookup"><span data-stu-id="85944-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="85944-108">Un'azione personalizzata per DllRegisterServer e una seconda per DllUnregisterServer.</span><span class="sxs-lookup"><span data-stu-id="85944-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="85944-109">Queste azioni personalizzate devono quindi essere create nella [tabella InstallExecuteSequence](installexecutesequence-table.md) in corrispondenza del punto della sequenza in cui deve essere registrata o annullata la registrazione della dll.</span><span class="sxs-lookup"><span data-stu-id="85944-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="85944-110">Nell'esempio seguente viene illustrato come creare il database per pianificare la registrazione automatica di una DLL in un determinato punto della sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="85944-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="85944-111">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="85944-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="85944-112">File</span><span class="sxs-lookup"><span data-stu-id="85944-112">File</span></span>  | <span data-ttu-id="85944-113">Componente\_</span><span class="sxs-lookup"><span data-stu-id="85944-113">Component\_</span></span> | <span data-ttu-id="85944-114">FileName</span><span class="sxs-lookup"><span data-stu-id="85944-114">FileName</span></span>  | <span data-ttu-id="85944-115">Sequenza</span><span class="sxs-lookup"><span data-stu-id="85944-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="85944-116">mydll</span><span class="sxs-lookup"><span data-stu-id="85944-116">mydll</span></span> | <span data-ttu-id="85944-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="85944-117">myComponent</span></span> | <span data-ttu-id="85944-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="85944-118">Mydll.dll</span></span> | <span data-ttu-id="85944-119">13</span><span class="sxs-lookup"><span data-stu-id="85944-119">13</span></span>       |



 

<span data-ttu-id="85944-120">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="85944-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="85944-121">Componente</span><span class="sxs-lookup"><span data-stu-id="85944-121">Component</span></span>   | <span data-ttu-id="85944-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="85944-122">ComponentId</span></span> | <span data-ttu-id="85944-123">Directory\_</span><span class="sxs-lookup"><span data-stu-id="85944-123">Directory\_</span></span> | <span data-ttu-id="85944-124">KeyPath</span><span class="sxs-lookup"><span data-stu-id="85944-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="85944-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="85944-125">myComponent</span></span> | <span data-ttu-id="85944-126">{*GUID*}</span><span class="sxs-lookup"><span data-stu-id="85944-126">{*a GUID*}</span></span>  | <span data-ttu-id="85944-127">myFolder</span><span class="sxs-lookup"><span data-stu-id="85944-127">myFolder</span></span>    | <span data-ttu-id="85944-128">mydll</span><span class="sxs-lookup"><span data-stu-id="85944-128">mydll</span></span>   |



 

[<span data-ttu-id="85944-129">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="85944-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="85944-130">Directory</span><span class="sxs-lookup"><span data-stu-id="85944-130">Directory</span></span> | <span data-ttu-id="85944-131">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="85944-131">Directory\_Parent</span></span> | <span data-ttu-id="85944-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="85944-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="85944-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="85944-133">TARGETDIR</span></span> |                   | <span data-ttu-id="85944-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="85944-134">SourceDir</span></span>           |
| <span data-ttu-id="85944-135">myFolder</span><span class="sxs-lookup"><span data-stu-id="85944-135">myFolder</span></span>  | <span data-ttu-id="85944-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="85944-136">TARGETDIR</span></span>         | <span data-ttu-id="85944-137">cartella \| My</span><span class="sxs-lookup"><span data-stu-id="85944-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="85944-138">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="85944-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="85944-139">Azione</span><span class="sxs-lookup"><span data-stu-id="85944-139">Action</span></span>     | <span data-ttu-id="85944-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="85944-140">Type</span></span> | <span data-ttu-id="85944-141">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="85944-141">Source</span></span>   | <span data-ttu-id="85944-142">Destinazione</span><span class="sxs-lookup"><span data-stu-id="85944-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="85944-143">mydllREG</span><span class="sxs-lookup"><span data-stu-id="85944-143">mydllREG</span></span>   | <span data-ttu-id="85944-144">3170</span><span class="sxs-lookup"><span data-stu-id="85944-144">3170</span></span> | <span data-ttu-id="85944-145">myFolder</span><span class="sxs-lookup"><span data-stu-id="85944-145">myFolder</span></span> | <span data-ttu-id="85944-146">" \[ SystemFolder \] msiexec"/y " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="85944-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="85944-147">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="85944-147">mydllUNREG</span></span> | <span data-ttu-id="85944-148">3170</span><span class="sxs-lookup"><span data-stu-id="85944-148">3170</span></span> | <span data-ttu-id="85944-149">myFolder</span><span class="sxs-lookup"><span data-stu-id="85944-149">myFolder</span></span> | <span data-ttu-id="85944-150">" \[ SystemFolder \] msiexec"/z " \[ \# myDll \] "</span><span class="sxs-lookup"><span data-stu-id="85944-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="85944-151">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="85944-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="85944-152">Azione</span><span class="sxs-lookup"><span data-stu-id="85944-152">Action</span></span>           | <span data-ttu-id="85944-153">Condizione</span><span class="sxs-lookup"><span data-stu-id="85944-153">Condition</span></span>         | <span data-ttu-id="85944-154">Sequenza</span><span class="sxs-lookup"><span data-stu-id="85944-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="85944-155">SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="85944-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="85944-156">2200</span><span class="sxs-lookup"><span data-stu-id="85944-156">2200</span></span>     |
| <span data-ttu-id="85944-157">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="85944-157">mydllUNREG</span></span>       | <span data-ttu-id="85944-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="85944-158">$myComponent=2</span></span>    | <span data-ttu-id="85944-159">2201</span><span class="sxs-lookup"><span data-stu-id="85944-159">2201</span></span>     |
| <span data-ttu-id="85944-160">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="85944-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="85944-161">3500</span><span class="sxs-lookup"><span data-stu-id="85944-161">3500</span></span>     |
| <span data-ttu-id="85944-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="85944-162">InstallFiles</span></span>     |                   | <span data-ttu-id="85944-163">4000</span><span class="sxs-lookup"><span data-stu-id="85944-163">4000</span></span>     |
| <span data-ttu-id="85944-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="85944-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="85944-165">6500</span><span class="sxs-lookup"><span data-stu-id="85944-165">6500</span></span>     |
| <span data-ttu-id="85944-166">mydllREG</span><span class="sxs-lookup"><span data-stu-id="85944-166">mydllREG</span></span>         | <span data-ttu-id="85944-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="85944-167">$myComponent>2</span></span> | <span data-ttu-id="85944-168">6501</span><span class="sxs-lookup"><span data-stu-id="85944-168">6501</span></span>     |



 

 

 



