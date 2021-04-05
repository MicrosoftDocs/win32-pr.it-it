---
description: Nella tabella AdvtExecuteSequence sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l'azione di annuncio di primo livello. Vedere il gruppo di tabelle delle procedure di installazione, usando una tabella di sequenza e l'esempio dettagliato della tabella di sequenza.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importazione del AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757817"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="a0242-104">Importazione del AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a0242-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="a0242-105">Nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md) sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l' [azione di annuncio](advertise-action.md)di primo livello.</span><span class="sxs-lookup"><span data-stu-id="a0242-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="a0242-106">Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="a0242-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="a0242-107">Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0242-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="a0242-108">Non è necessario apportare modifiche a queste sequenze per creare il pacchetto di installazione di esempio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="a0242-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="a0242-109">Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0242-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="a0242-110">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a0242-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="a0242-111">Azione</span><span class="sxs-lookup"><span data-stu-id="a0242-111">Action</span></span>                | <span data-ttu-id="a0242-112">Condizione</span><span class="sxs-lookup"><span data-stu-id="a0242-112">Condition</span></span> | <span data-ttu-id="a0242-113">Sequenza</span><span class="sxs-lookup"><span data-stu-id="a0242-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="a0242-114">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="a0242-114">CostFinalize</span></span>          |           | <span data-ttu-id="a0242-115">1000</span><span class="sxs-lookup"><span data-stu-id="a0242-115">1000</span></span>     |
| <span data-ttu-id="a0242-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="a0242-116">CostInitialize</span></span>        |           | <span data-ttu-id="a0242-117">800</span><span class="sxs-lookup"><span data-stu-id="a0242-117">800</span></span>      |
| <span data-ttu-id="a0242-118">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="a0242-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="a0242-119">4500</span><span class="sxs-lookup"><span data-stu-id="a0242-119">4500</span></span>     |
| <span data-ttu-id="a0242-120">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="a0242-120">InstallFinalize</span></span>       |           | <span data-ttu-id="a0242-121">6600</span><span class="sxs-lookup"><span data-stu-id="a0242-121">6600</span></span>     |
| <span data-ttu-id="a0242-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="a0242-122">InstallInitialize</span></span>     |           | <span data-ttu-id="a0242-123">1500</span><span class="sxs-lookup"><span data-stu-id="a0242-123">1500</span></span>     |
| <span data-ttu-id="a0242-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="a0242-124">InstallValidate</span></span>       |           | <span data-ttu-id="a0242-125">1400</span><span class="sxs-lookup"><span data-stu-id="a0242-125">1400</span></span>     |
| <span data-ttu-id="a0242-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="a0242-126">PublishComponents</span></span>     |           | <span data-ttu-id="a0242-127">6200</span><span class="sxs-lookup"><span data-stu-id="a0242-127">6200</span></span>     |
| <span data-ttu-id="a0242-128">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="a0242-128">PublishFeatures</span></span>       |           | <span data-ttu-id="a0242-129">6300</span><span class="sxs-lookup"><span data-stu-id="a0242-129">6300</span></span>     |
| <span data-ttu-id="a0242-130">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="a0242-130">PublishProduct</span></span>        |           | <span data-ttu-id="a0242-131">6400</span><span class="sxs-lookup"><span data-stu-id="a0242-131">6400</span></span>     |
| <span data-ttu-id="a0242-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="a0242-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="a0242-133">4600</span><span class="sxs-lookup"><span data-stu-id="a0242-133">4600</span></span>     |
| <span data-ttu-id="a0242-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="a0242-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="a0242-135">4700</span><span class="sxs-lookup"><span data-stu-id="a0242-135">4700</span></span>     |
| <span data-ttu-id="a0242-136">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="a0242-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="a0242-137">4900</span><span class="sxs-lookup"><span data-stu-id="a0242-137">4900</span></span>     |
| <span data-ttu-id="a0242-138">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="a0242-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="a0242-139">4800</span><span class="sxs-lookup"><span data-stu-id="a0242-139">4800</span></span>     |



 

<span data-ttu-id="a0242-140">La [tabella AdvtUISequence](advtuisequence-table.md) non viene utilizzata dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="a0242-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="a0242-141">Questa tabella non deve esistere o essere lasciata vuota nel database di installazione.</span><span class="sxs-lookup"><span data-stu-id="a0242-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="a0242-142">Continua</span><span class="sxs-lookup"><span data-stu-id="a0242-142">Continue</span></span>](adding-summary-information.md)

 

 



