---
description: Nella tabella AdminUISequence sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l'azione di amministrazione di livello superiore e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importazione del AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314783"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="9f849-103">Importazione del AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="9f849-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="9f849-104">Nella [tabella AdminUISequence](adminuisequence-table.md) sono elencate le azioni chiamate dal programma di installazione quando viene eseguita l' [azione di amministrazione](admin-action.md) di livello superiore e il livello dell'interfaccia utente interna è impostato su interfaccia utente completa o interfaccia utente ridotta.</span><span class="sxs-lookup"><span data-stu-id="9f849-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="9f849-105">Il programma di installazione ignora le azioni in questa tabella se il livello dell'interfaccia utente è impostato su interfaccia utente di base o nessuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="9f849-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="9f849-106">Vedere livelli di [interfaccia utente e](user-interface.md) [interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9f849-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="9f849-107">Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="9f849-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="9f849-108">Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="9f849-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="9f849-109">Non è necessario apportare modifiche a queste sequenze per installare l'esempio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="9f849-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="9f849-110">Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="9f849-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="9f849-111">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="9f849-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="9f849-112">Azione</span><span class="sxs-lookup"><span data-stu-id="9f849-112">Action</span></span>          | <span data-ttu-id="9f849-113">Condizione</span><span class="sxs-lookup"><span data-stu-id="9f849-113">Condition</span></span> | <span data-ttu-id="9f849-114">Sequenza</span><span class="sxs-lookup"><span data-stu-id="9f849-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="9f849-115">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="9f849-116">1230</span><span class="sxs-lookup"><span data-stu-id="9f849-116">1230</span></span>     |
| <span data-ttu-id="9f849-117">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="9f849-117">CostFinalize</span></span>    |           | <span data-ttu-id="9f849-118">1000</span><span class="sxs-lookup"><span data-stu-id="9f849-118">1000</span></span>     |
| <span data-ttu-id="9f849-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="9f849-119">CostInitialize</span></span>  |           | <span data-ttu-id="9f849-120">800</span><span class="sxs-lookup"><span data-stu-id="9f849-120">800</span></span>      |
| <span data-ttu-id="9f849-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="9f849-121">ExecuteAction</span></span>   |           | <span data-ttu-id="9f849-122">1300</span><span class="sxs-lookup"><span data-stu-id="9f849-122">1300</span></span>     |
| <span data-ttu-id="9f849-123">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-123">ExitDlg</span></span>         |           | <span data-ttu-id="9f849-124">-1</span><span class="sxs-lookup"><span data-stu-id="9f849-124">-1</span></span>       |
| <span data-ttu-id="9f849-125">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="9f849-126">-3</span><span class="sxs-lookup"><span data-stu-id="9f849-126">-3</span></span>       |
| <span data-ttu-id="9f849-127">Filecost</span><span class="sxs-lookup"><span data-stu-id="9f849-127">FileCost</span></span>        |           | <span data-ttu-id="9f849-128">900</span><span class="sxs-lookup"><span data-stu-id="9f849-128">900</span></span>      |
| <span data-ttu-id="9f849-129">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-129">PrepareDlg</span></span>      |           | <span data-ttu-id="9f849-130">140</span><span class="sxs-lookup"><span data-stu-id="9f849-130">140</span></span>      |
| <span data-ttu-id="9f849-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-131">ProgressDlg</span></span>     |           | <span data-ttu-id="9f849-132">1280</span><span class="sxs-lookup"><span data-stu-id="9f849-132">1280</span></span>     |
| <span data-ttu-id="9f849-133">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="9f849-133">UserExitDlg</span></span>     |           | <span data-ttu-id="9f849-134">-2</span><span class="sxs-lookup"><span data-stu-id="9f849-134">-2</span></span>       |



 

[<span data-ttu-id="9f849-135">Continua</span><span class="sxs-lookup"><span data-stu-id="9f849-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



