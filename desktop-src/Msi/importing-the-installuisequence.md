---
description: La sequenza dell'interfaccia utente viene importata nel database di esempio.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importazione del InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232441"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="a5734-103">Importazione del InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="a5734-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="a5734-104">Nella [tabella InstallUISequence](installuisequence-table.md) sono elencate le azioni che vengono eseguite quando viene eseguita l' [azione di installazione](install-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato sull'interfaccia utente completa o sull'interfaccia utente ridotta.</span><span class="sxs-lookup"><span data-stu-id="a5734-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="a5734-105">Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato sull'interfaccia utente di base o su nessuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a5734-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="a5734-106">Vedere livelli di [interfaccia utente e](user-interface.md) [interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a5734-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="a5734-107">Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="a5734-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="a5734-108">Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a5734-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="a5734-109">Per creare il pacchetto di installazione del blocco note non è necessario apportare modifiche a tali sequenze.</span><span class="sxs-lookup"><span data-stu-id="a5734-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="a5734-110">Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="a5734-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="a5734-111">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="a5734-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="a5734-112">Azione</span><span class="sxs-lookup"><span data-stu-id="a5734-112">Action</span></span>                | <span data-ttu-id="a5734-113">Condizione</span><span class="sxs-lookup"><span data-stu-id="a5734-113">Condition</span></span>                                    | <span data-ttu-id="a5734-114">Sequenza</span><span class="sxs-lookup"><span data-stu-id="a5734-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="a5734-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="a5734-115">AppSearch</span></span>             |                                              | <span data-ttu-id="a5734-116">400</span><span class="sxs-lookup"><span data-stu-id="a5734-116">400</span></span>      |
| <span data-ttu-id="a5734-117">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="a5734-117">CCPSearch</span></span>             | <span data-ttu-id="a5734-118">NON installato</span><span class="sxs-lookup"><span data-stu-id="a5734-118">NOT Installed</span></span>                                | <span data-ttu-id="a5734-119">500</span><span class="sxs-lookup"><span data-stu-id="a5734-119">500</span></span>      |
| <span data-ttu-id="a5734-120">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="a5734-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="a5734-121">1000</span><span class="sxs-lookup"><span data-stu-id="a5734-121">1000</span></span>     |
| <span data-ttu-id="a5734-122">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="a5734-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="a5734-123">800</span><span class="sxs-lookup"><span data-stu-id="a5734-123">800</span></span>      |
| <span data-ttu-id="a5734-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="a5734-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="a5734-125">1300</span><span class="sxs-lookup"><span data-stu-id="a5734-125">1300</span></span>     |
| <span data-ttu-id="a5734-126">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="a5734-127">-1</span><span class="sxs-lookup"><span data-stu-id="a5734-127">-1</span></span>       |
| <span data-ttu-id="a5734-128">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="a5734-129">-3</span><span class="sxs-lookup"><span data-stu-id="a5734-129">-3</span></span>       |
| <span data-ttu-id="a5734-130">Filecost</span><span class="sxs-lookup"><span data-stu-id="a5734-130">FileCost</span></span>              |                                              | <span data-ttu-id="a5734-131">900</span><span class="sxs-lookup"><span data-stu-id="a5734-131">900</span></span>      |
| <span data-ttu-id="a5734-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="a5734-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="a5734-133">100</span><span class="sxs-lookup"><span data-stu-id="a5734-133">100</span></span>      |
| <span data-ttu-id="a5734-134">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="a5734-135">Installato e non ripreso e non preselezionato</span><span class="sxs-lookup"><span data-stu-id="a5734-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="a5734-136">1250</span><span class="sxs-lookup"><span data-stu-id="a5734-136">1250</span></span>     |
| <span data-ttu-id="a5734-137">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="a5734-138">140</span><span class="sxs-lookup"><span data-stu-id="a5734-138">140</span></span>      |
| <span data-ttu-id="a5734-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="a5734-140">1280</span><span class="sxs-lookup"><span data-stu-id="a5734-140">1280</span></span>     |
| <span data-ttu-id="a5734-141">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-141">ResumeDlg</span></span>             | <span data-ttu-id="a5734-142">Installato e (ripresa o preselezione)</span><span class="sxs-lookup"><span data-stu-id="a5734-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="a5734-143">1240</span><span class="sxs-lookup"><span data-stu-id="a5734-143">1240</span></span>     |
| <span data-ttu-id="a5734-144">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="a5734-144">RMCCPSearch</span></span>           | <span data-ttu-id="a5734-145">NON installato</span><span class="sxs-lookup"><span data-stu-id="a5734-145">NOT Installed</span></span>                                | <span data-ttu-id="a5734-146">600</span><span class="sxs-lookup"><span data-stu-id="a5734-146">600</span></span>      |
| <span data-ttu-id="a5734-147">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="a5734-148">-2</span><span class="sxs-lookup"><span data-stu-id="a5734-148">-2</span></span>       |
| <span data-ttu-id="a5734-149">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="a5734-149">WelcomeDlg</span></span>            | <span data-ttu-id="a5734-150">NON installato</span><span class="sxs-lookup"><span data-stu-id="a5734-150">NOT Installed</span></span>                                | <span data-ttu-id="a5734-151">1230</span><span class="sxs-lookup"><span data-stu-id="a5734-151">1230</span></span>     |
| <span data-ttu-id="a5734-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="a5734-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="a5734-153">1200</span><span class="sxs-lookup"><span data-stu-id="a5734-153">1200</span></span>     |
| <span data-ttu-id="a5734-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="a5734-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="a5734-155">200</span><span class="sxs-lookup"><span data-stu-id="a5734-155">200</span></span>      |



 

[<span data-ttu-id="a5734-156">Continua</span><span class="sxs-lookup"><span data-stu-id="a5734-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



