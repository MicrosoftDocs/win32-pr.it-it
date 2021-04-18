---
description: ICE12 convalida le tabelle CustomAction, directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence e InstallUISequence del database Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314238"
---
# <a name="ice12"></a><span data-ttu-id="b2452-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="b2452-103">ICE12</span></span>

<span data-ttu-id="b2452-104">ICE12 esegue una query sulle tabelle [CustomAction](customaction-table.md), [directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)e [InstallUISequence](installuisequence-table.md) per convalidare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="b2452-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="b2452-105">L' [azione CostFinalize secondo](costfinalize-action.md) si verifica in qualsiasi tabella di sequenza contenente azioni del tipo di [azione personalizzata 35](custom-action-type-35.md) o [tipo di azione personalizzata 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="b2452-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="b2452-106">Ogni [tipo di azione personalizzata 35](custom-action-type-35.md) viene eseguito dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b2452-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="b2452-107">nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="b2452-107">in the sequence tables.</span></span>
-   <span data-ttu-id="b2452-108">Ogni [tipo di azione personalizzata 51](custom-action-type-51.md) che dispone di una chiave esterna per la tabella di directory nella colonna di origine della tabella CustomAction precede l' [azione CostFinalize secondo](costfinalize-action.md) nelle tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="b2452-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="b2452-109">Si noti che ICE12 non convalida il testo formattato nella colonna di destinazione della tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="b2452-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="b2452-110">Risultato</span><span class="sxs-lookup"><span data-stu-id="b2452-110">Result</span></span>

<span data-ttu-id="b2452-111">ICE12 Invia un messaggio di errore se la convalida delle azioni personalizzate che impostano una proprietà della directory ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b2452-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="b2452-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2452-112">Example</span></span>

<span data-ttu-id="b2452-113">ICE12 avrebbe pubblicato tre errori per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="b2452-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="b2452-114">Per CA1, la cartella ' fileFolder ' non è stata trovata nella tabella di directory</span><span class="sxs-lookup"><span data-stu-id="b2452-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="b2452-115">Per il CA2, la sequenza '80 ' precede CostFinalize secondo nella tabella InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="b2452-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="b2452-116">Deve essere successiva a ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="b2452-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="b2452-117">Per CA3, la sequenza ' 125' è successiva a CostFinalize secondo nella tabella InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="b2452-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="b2452-118">Deve precedere ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="b2452-118">It must come before (CF@100)</span></span>

<span data-ttu-id="b2452-119">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b2452-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="b2452-120">Azione</span><span class="sxs-lookup"><span data-stu-id="b2452-120">Action</span></span> | <span data-ttu-id="b2452-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2452-121">Type</span></span> | <span data-ttu-id="b2452-122">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="b2452-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="b2452-123">CA1</span><span class="sxs-lookup"><span data-stu-id="b2452-123">CA1</span></span>    | <span data-ttu-id="b2452-124">35</span><span class="sxs-lookup"><span data-stu-id="b2452-124">35</span></span>   | <span data-ttu-id="b2452-125">MyFolder</span><span class="sxs-lookup"><span data-stu-id="b2452-125">MyFolder</span></span>      |
| <span data-ttu-id="b2452-126">CA2</span><span class="sxs-lookup"><span data-stu-id="b2452-126">CA2</span></span>    | <span data-ttu-id="b2452-127">35</span><span class="sxs-lookup"><span data-stu-id="b2452-127">35</span></span>   | <span data-ttu-id="b2452-128">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="b2452-128">WindowsFolder</span></span> |
| <span data-ttu-id="b2452-129">CA3</span><span class="sxs-lookup"><span data-stu-id="b2452-129">CA3</span></span>    | <span data-ttu-id="b2452-130">51</span><span class="sxs-lookup"><span data-stu-id="b2452-130">51</span></span>   | <span data-ttu-id="b2452-131">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="b2452-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="b2452-132">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="b2452-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="b2452-133">Directory</span><span class="sxs-lookup"><span data-stu-id="b2452-133">Directory</span></span>     | <span data-ttu-id="b2452-134">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="b2452-134">Directory\_Parent</span></span> | <span data-ttu-id="b2452-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b2452-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="b2452-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b2452-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="b2452-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="b2452-137">SourceDir</span></span>     |
| <span data-ttu-id="b2452-138">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="b2452-138">WindowsFolder</span></span> | <span data-ttu-id="b2452-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b2452-139">TARGETDIR</span></span>         | <span data-ttu-id="b2452-140">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="b2452-140">WindowsFolder</span></span> |



 

<span data-ttu-id="b2452-141">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b2452-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="b2452-142">Azione</span><span class="sxs-lookup"><span data-stu-id="b2452-142">Action</span></span>       | <span data-ttu-id="b2452-143">Sequenza</span><span class="sxs-lookup"><span data-stu-id="b2452-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="b2452-144">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="b2452-144">CostFinalize</span></span> | <span data-ttu-id="b2452-145">100</span><span class="sxs-lookup"><span data-stu-id="b2452-145">100</span></span>      |
| <span data-ttu-id="b2452-146">CA2</span><span class="sxs-lookup"><span data-stu-id="b2452-146">CA2</span></span>          | <span data-ttu-id="b2452-147">80</span><span class="sxs-lookup"><span data-stu-id="b2452-147">80</span></span>       |
| <span data-ttu-id="b2452-148">CA3</span><span class="sxs-lookup"><span data-stu-id="b2452-148">CA3</span></span>          | <span data-ttu-id="b2452-149">125</span><span class="sxs-lookup"><span data-stu-id="b2452-149">125</span></span>      |



 

<span data-ttu-id="b2452-150">Per correggere l'errore per CA1, modificare la voce della relativa colonna di origine nella tabella CustomAction con una voce esistente nella tabella directory o aggiungere la cartella alla tabella directory.</span><span class="sxs-lookup"><span data-stu-id="b2452-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="b2452-151">Per correggere l'errore per CA2, modificare la relativa sequenza nella tabella InstallExecuteSequence in modo che venga eseguita dopo l'azione CostFinalize secondo.</span><span class="sxs-lookup"><span data-stu-id="b2452-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="b2452-152">Per correggere l'errore per CA3, modificare la relativa sequenza nella tabella InstallExecuteSequence in modo che venga prima dell'azione CostFinalize secondo.</span><span class="sxs-lookup"><span data-stu-id="b2452-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2452-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b2452-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2452-154">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b2452-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



