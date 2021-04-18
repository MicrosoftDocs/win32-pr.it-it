---
description: ICEM04 verifica che le tabelle vuote obbligatorie del modulo merge siano vuote. Impossibile correggere un errore per il quale i report di ICEM04 possono causare un merge errato del modulo merge.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308686"
---
# <a name="icem04"></a><span data-ttu-id="32c70-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="32c70-104">ICEM04</span></span>

<span data-ttu-id="32c70-105">ICEM04 verifica che le tabelle vuote obbligatorie del modulo merge siano vuote.</span><span class="sxs-lookup"><span data-stu-id="32c70-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="32c70-106">Impossibile correggere un errore per il quale i report di ICEM04 possono causare un merge errato del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="32c70-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="32c70-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="32c70-107">Result</span></span>

<span data-ttu-id="32c70-108">ICEM04 Invia un errore quando le tabelle vuote richieste del modulo merge non sono vuote.</span><span class="sxs-lookup"><span data-stu-id="32c70-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="32c70-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="32c70-109">Example</span></span>

<span data-ttu-id="32c70-110">ICEM04 invia i messaggi di errore seguenti per un modulo che contiene le voci di database indicate.</span><span class="sxs-lookup"><span data-stu-id="32c70-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="32c70-111">Nella tabella seguente viene illustrata una [tabella AdvtExecuteSequence](advtexecutesequence-table.md)parziale.</span><span class="sxs-lookup"><span data-stu-id="32c70-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="32c70-112">Azione</span><span class="sxs-lookup"><span data-stu-id="32c70-112">Action</span></span>         | <span data-ttu-id="32c70-113">Sequenza</span><span class="sxs-lookup"><span data-stu-id="32c70-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="32c70-114">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="32c70-114">CostInitialize</span></span> | <span data-ttu-id="32c70-115">1</span><span class="sxs-lookup"><span data-stu-id="32c70-115">1</span></span>        |



 

<span data-ttu-id="32c70-116">Nell'elenco seguente viene illustrato il contenuto parziale di MergeModule:</span><span class="sxs-lookup"><span data-stu-id="32c70-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="32c70-117">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="32c70-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="32c70-118">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="32c70-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="32c70-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="32c70-119">InstallUISequence</span></span>

<span data-ttu-id="32c70-120">Nell'esempio seguente viene illustrato un altro errore possibile.</span><span class="sxs-lookup"><span data-stu-id="32c70-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="32c70-121">Se un modulo merge contiene una tabella di sequenza dei moduli, deve contenere la tabella di sequenza vuota corrispondente, indipendentemente dal fatto che la tabella di sequenza dei moduli sia vuota o meno.</span><span class="sxs-lookup"><span data-stu-id="32c70-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="32c70-122">Se, ad esempio, il modulo merge contiene la [tabella ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), è necessario che contenga anche una tabella AdminExecuteSequence vuota.</span><span class="sxs-lookup"><span data-stu-id="32c70-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="32c70-123">La [tabella FeatureComponents](featurecomponents-table.md) è obbligatoria in tutti i moduli merge e deve essere vuota.</span><span class="sxs-lookup"><span data-stu-id="32c70-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="32c70-124">Nella procedura riportata di seguito viene illustrato come correggere gli errori.</span><span class="sxs-lookup"><span data-stu-id="32c70-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="32c70-125">**Per correggere gli errori**</span><span class="sxs-lookup"><span data-stu-id="32c70-125">**To fix errors**</span></span>

1.  <span data-ttu-id="32c70-126">Aggiungere una [tabella FeatureComponents](featurecomponents-table.md) vuota al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="32c70-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="32c70-127">Aggiungere una [tabella InstallExecuteSequence](installexecutesequence-table.md) vuota al modulo merge.</span><span class="sxs-lookup"><span data-stu-id="32c70-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="32c70-128">Rimuovere l'azione ' CostInitialize ' dalla [tabella AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="32c70-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="32c70-129">Questa tabella deve essere vuota in un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="32c70-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="32c70-130">Le azioni devono essere visualizzate solo nella tabella ModuleAdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="32c70-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="32c70-131">Tabelle utilizzate durante l'esecuzione</span><span class="sxs-lookup"><span data-stu-id="32c70-131">Tables Used During Execution</span></span>

<span data-ttu-id="32c70-132">Nell'elenco seguente vengono identificate le tabelle utilizzate durante l'esecuzione:</span><span class="sxs-lookup"><span data-stu-id="32c70-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="32c70-133">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="32c70-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="32c70-134">\*Tabelle di sequenza del modulo e \* tabelle di sequenza corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="32c70-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c70-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32c70-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c70-136">Informazioni sui moduli merge</span><span class="sxs-lookup"><span data-stu-id="32c70-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="32c70-137">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="32c70-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



