---
description: ICE77 verifica che le azioni personalizzate con il set di bit msidbCustomActionTypeInScript vengano sequenziate dopo l'azione InstallInitialize e prima dell'azione InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129971"
---
# <a name="ice77"></a><span data-ttu-id="27507-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="27507-103">ICE77</span></span>

<span data-ttu-id="27507-104">ICE77 verifica che le azioni personalizzate con il set di bit **msidbCustomActionTypeInScript** vengano sequenziate dopo l' [azione InstallInitialize](installinitialize-action.md) e prima dell' [azione InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="27507-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="27507-105">ICE77 verifica la sequenza nella tabella [InstallExecuteSequence](installexecutesequence-table.md) e nella [tabella AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="27507-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="27507-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="27507-106">Result</span></span>

<span data-ttu-id="27507-107">ICE77 Invia un errore se un'azione personalizzata nello script viene sequenziata prima dell'azione InstallInitialize o dopo l'azione InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="27507-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="27507-108">ICE77 Invia un errore se l'azione InstallInitialize o InstallFinalize è mancante.</span><span class="sxs-lookup"><span data-stu-id="27507-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="27507-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="27507-109">Example</span></span>

<span data-ttu-id="27507-110">ICE77 segnala gli errori seguenti per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="27507-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="27507-111">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27507-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="27507-112">Azione</span><span class="sxs-lookup"><span data-stu-id="27507-112">Action</span></span>              | <span data-ttu-id="27507-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="27507-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="27507-114">\_INSCRIPTINSTALL CA</span><span class="sxs-lookup"><span data-stu-id="27507-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="27507-115">1025</span><span class="sxs-lookup"><span data-stu-id="27507-115">1025</span></span> |
| <span data-ttu-id="27507-116">\_INSCRIPTADMIN CA</span><span class="sxs-lookup"><span data-stu-id="27507-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="27507-117">1026</span><span class="sxs-lookup"><span data-stu-id="27507-117">1026</span></span> |



 

<span data-ttu-id="27507-118">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27507-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="27507-119">Azione</span><span class="sxs-lookup"><span data-stu-id="27507-119">Action</span></span>              | <span data-ttu-id="27507-120">Sequenza</span><span class="sxs-lookup"><span data-stu-id="27507-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="27507-121">\_INSCRIPTINSTALL CA</span><span class="sxs-lookup"><span data-stu-id="27507-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="27507-122">2000</span><span class="sxs-lookup"><span data-stu-id="27507-122">2000</span></span>     |
| <span data-ttu-id="27507-123">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="27507-123">InstallInitialize</span></span>   | <span data-ttu-id="27507-124">1500</span><span class="sxs-lookup"><span data-stu-id="27507-124">1500</span></span>     |



 

<span data-ttu-id="27507-125">[Tabella AdminExecuteSequence](adminexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="27507-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="27507-126">Azione</span><span class="sxs-lookup"><span data-stu-id="27507-126">Action</span></span>            | <span data-ttu-id="27507-127">Sequenza</span><span class="sxs-lookup"><span data-stu-id="27507-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="27507-128">\_INSCRIPTADMIN CA</span><span class="sxs-lookup"><span data-stu-id="27507-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="27507-129">1400</span><span class="sxs-lookup"><span data-stu-id="27507-129">1400</span></span>     |
| <span data-ttu-id="27507-130">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="27507-130">InstallInitialize</span></span> | <span data-ttu-id="27507-131">1500</span><span class="sxs-lookup"><span data-stu-id="27507-131">1500</span></span>     |
| <span data-ttu-id="27507-132">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="27507-132">InstallFinalize</span></span>   | <span data-ttu-id="27507-133">6600</span><span class="sxs-lookup"><span data-stu-id="27507-133">6600</span></span>     |



 

<span data-ttu-id="27507-134">Per correggere gli errori, sequenziare le azioni personalizzate nello script dopo l'azione InstallInitialize e prima dell'azione InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="27507-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="27507-135">Le azioni InstallInitialize e InstallFinalize devono essere presenti nella tabella InstallExecuteSequence e nella tabella AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="27507-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27507-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27507-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27507-137">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="27507-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



