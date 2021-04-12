---
description: ICE75 verifica che tutte le azioni personalizzate 17 (DLL), tipo di azione personalizzata 18 (EXE), tipo di azione personalizzata 21 (JScript) e tipo di azione personalizzata 22 (VBScript) vengano sequenziate dopo l'azione CostFinalize secondo.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347356"
---
# <a name="ice75"></a><span data-ttu-id="63525-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="63525-103">ICE75</span></span>

<span data-ttu-id="63525-104">ICE75 verifica che tutte le azioni personalizzate [17](custom-action-type-17.md) (dll), tipo [di azione personalizzata 18](custom-action-type-18.md) (exe), [tipo](custom-action-type-21.md) di azione personalizzata 21 (JScript) e [tipo di azione personalizzata 22](custom-action-type-22.md) (VBScript) vengano sequenziate dopo l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="63525-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="63525-105">Questi tipi di azione personalizzata utilizzano un file installato come origine.</span><span class="sxs-lookup"><span data-stu-id="63525-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="63525-106">ICE75 controlla la tabella [InstallUISequence](installuisequence-table.md), la tabella [InstallExecuteSequence](installexecutesequence-table.md), la tabella [AdminUISequence](adminuisequence-table.md)e la [tabella AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="63525-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="63525-107">Si noti che l'azione CostFinalize secondo è obbligatoria in queste tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="63525-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="63525-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="63525-108">Result</span></span>

<span data-ttu-id="63525-109">ICE75 Invia un errore se trova un'azione personalizzata usando un file installato come file di origine che non è sequenziato dopo l'azione CostFinalize secondo.</span><span class="sxs-lookup"><span data-stu-id="63525-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="63525-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="63525-110">Example</span></span>

<span data-ttu-id="63525-111">ICE75 segnala gli errori seguenti per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="63525-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="63525-112">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="63525-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="63525-113">Azione</span><span class="sxs-lookup"><span data-stu-id="63525-113">Action</span></span>      | <span data-ttu-id="63525-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="63525-114">Type</span></span> | <span data-ttu-id="63525-115">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="63525-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="63525-116">\_FILEEXE CA</span><span class="sxs-lookup"><span data-stu-id="63525-116">CA\_FileExe</span></span> | <span data-ttu-id="63525-117">18</span><span class="sxs-lookup"><span data-stu-id="63525-117">18</span></span>   | <span data-ttu-id="63525-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="63525-118">FileExe</span></span> |
| <span data-ttu-id="63525-119">\_FILEDLL CA</span><span class="sxs-lookup"><span data-stu-id="63525-119">CA\_FileDLL</span></span> | <span data-ttu-id="63525-120">17</span><span class="sxs-lookup"><span data-stu-id="63525-120">17</span></span>   | <span data-ttu-id="63525-121">FileDLL</span><span class="sxs-lookup"><span data-stu-id="63525-121">FileDLL</span></span> |



 

<span data-ttu-id="63525-122">[Tabella AdminUISequence](adminuisequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="63525-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="63525-123">Azione</span><span class="sxs-lookup"><span data-stu-id="63525-123">Action</span></span>      | <span data-ttu-id="63525-124">Sequenza</span><span class="sxs-lookup"><span data-stu-id="63525-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="63525-125">\_FILEEXE CA</span><span class="sxs-lookup"><span data-stu-id="63525-125">CA\_FileExe</span></span> | <span data-ttu-id="63525-126">1100</span><span class="sxs-lookup"><span data-stu-id="63525-126">1100</span></span>     |



 

<span data-ttu-id="63525-127">[Tabella AdminExecuteSequence](adminexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="63525-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="63525-128">Azione</span><span class="sxs-lookup"><span data-stu-id="63525-128">Action</span></span>       | <span data-ttu-id="63525-129">Sequenza</span><span class="sxs-lookup"><span data-stu-id="63525-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="63525-130">\_FILEDLL CA</span><span class="sxs-lookup"><span data-stu-id="63525-130">CA\_FileDLL</span></span>  | <span data-ttu-id="63525-131">800</span><span class="sxs-lookup"><span data-stu-id="63525-131">800</span></span>      |
| <span data-ttu-id="63525-132">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="63525-132">CostFinalize</span></span> | <span data-ttu-id="63525-133">1000</span><span class="sxs-lookup"><span data-stu-id="63525-133">1000</span></span>     |



 

<span data-ttu-id="63525-134">Per correggere gli errori, sequenziare le azioni personalizzate dopo l'azione CostFinalize secondo.</span><span class="sxs-lookup"><span data-stu-id="63525-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63525-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63525-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63525-136">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="63525-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



