---
description: Nella tabella AdminExecuteSequence sono elencate le azioni eseguite dal programma di installazione quando viene chiamata l'azione di amministrazione di primo livello. Vedere il gruppo di tabelle delle procedure di installazione, usando una tabella di sequenza e l'esempio dettagliato della tabella di sequenza.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importazione del AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752783"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="da2db-104">Importazione del AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="da2db-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="da2db-105">Nella [tabella AdminExecuteSequence](adminexecutesequence-table.md) sono elencate le azioni eseguite dal programma di installazione quando viene chiamata l' [azione di amministrazione](admin-action.md)di primo livello.</span><span class="sxs-lookup"><span data-stu-id="da2db-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="da2db-106">Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).</span><span class="sxs-lookup"><span data-stu-id="da2db-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="da2db-107">Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="da2db-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="da2db-108">Non è necessario apportare modifiche a queste sequenze per creare il pacchetto di installazione di esempio del blocco note.</span><span class="sxs-lookup"><span data-stu-id="da2db-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="da2db-109">Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="da2db-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="da2db-110">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="da2db-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="da2db-111">Azione</span><span class="sxs-lookup"><span data-stu-id="da2db-111">Action</span></span>              | <span data-ttu-id="da2db-112">Condizione</span><span class="sxs-lookup"><span data-stu-id="da2db-112">Condition</span></span> | <span data-ttu-id="da2db-113">Sequenza</span><span class="sxs-lookup"><span data-stu-id="da2db-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="da2db-114">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="da2db-114">CostFinalize</span></span>        |           | <span data-ttu-id="da2db-115">1000</span><span class="sxs-lookup"><span data-stu-id="da2db-115">1000</span></span>     |
| <span data-ttu-id="da2db-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="da2db-116">CostInitialize</span></span>      |           | <span data-ttu-id="da2db-117">800</span><span class="sxs-lookup"><span data-stu-id="da2db-117">800</span></span>      |
| <span data-ttu-id="da2db-118">Filecost</span><span class="sxs-lookup"><span data-stu-id="da2db-118">FileCost</span></span>            |           | <span data-ttu-id="da2db-119">900</span><span class="sxs-lookup"><span data-stu-id="da2db-119">900</span></span>      |
| <span data-ttu-id="da2db-120">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="da2db-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="da2db-121">3900</span><span class="sxs-lookup"><span data-stu-id="da2db-121">3900</span></span>     |
| <span data-ttu-id="da2db-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="da2db-122">InstallFiles</span></span>        |           | <span data-ttu-id="da2db-123">4000</span><span class="sxs-lookup"><span data-stu-id="da2db-123">4000</span></span>     |
| <span data-ttu-id="da2db-124">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="da2db-124">InstallFinalize</span></span>     |           | <span data-ttu-id="da2db-125">6600</span><span class="sxs-lookup"><span data-stu-id="da2db-125">6600</span></span>     |
| <span data-ttu-id="da2db-126">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="da2db-126">InstallInitialize</span></span>   |           | <span data-ttu-id="da2db-127">1500</span><span class="sxs-lookup"><span data-stu-id="da2db-127">1500</span></span>     |
| <span data-ttu-id="da2db-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="da2db-128">InstallValidate</span></span>     |           | <span data-ttu-id="da2db-129">1400</span><span class="sxs-lookup"><span data-stu-id="da2db-129">1400</span></span>     |



 

[<span data-ttu-id="da2db-130">Continua</span><span class="sxs-lookup"><span data-stu-id="da2db-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



