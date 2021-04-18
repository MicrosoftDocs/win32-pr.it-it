---
description: ICEM03 verifica che tutte le azioni del modulo siano azioni di base o derivano da un'azione di base valida.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313345"
---
# <a name="icem03"></a><span data-ttu-id="a8e78-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="a8e78-103">ICEM03</span></span>

<span data-ttu-id="a8e78-104">ICEM03 verifica che tutte le azioni del modulo siano azioni di base o derivano da un'azione di base valida.</span><span class="sxs-lookup"><span data-stu-id="a8e78-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="a8e78-105">I moduli CIEM di tipo merge vengono archiviati in un file con estensione cub del modulo merge denominato Mergemod. cub e non nel file con estensione cub contenente i ghiacci utilizzati per la convalida del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a8e78-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="a8e78-106">Risultato</span><span class="sxs-lookup"><span data-stu-id="a8e78-106">Result</span></span>

<span data-ttu-id="a8e78-107">ICEM03 invia i messaggi di errore per un modulo contenente azioni in una tabella di sequenza che non è un'azione di base o derivata da un'azione di base valida.</span><span class="sxs-lookup"><span data-stu-id="a8e78-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="a8e78-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8e78-108">Example</span></span>

<span data-ttu-id="a8e78-109">ICEM03 invia i messaggi di errore seguenti per un modulo contenente le voci di database indicate di seguito.</span><span class="sxs-lookup"><span data-stu-id="a8e78-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="a8e78-110">Tabella ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="a8e78-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="a8e78-111">Azione</span><span class="sxs-lookup"><span data-stu-id="a8e78-111">Action</span></span>  | <span data-ttu-id="a8e78-112">Sequenza</span><span class="sxs-lookup"><span data-stu-id="a8e78-112">Sequence</span></span> | <span data-ttu-id="a8e78-113">BaseAction</span><span class="sxs-lookup"><span data-stu-id="a8e78-113">BaseAction</span></span> | <span data-ttu-id="a8e78-114">After</span><span class="sxs-lookup"><span data-stu-id="a8e78-114">After</span></span> | <span data-ttu-id="a8e78-115">Condizione</span><span class="sxs-lookup"><span data-stu-id="a8e78-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="a8e78-116">Action1</span><span class="sxs-lookup"><span data-stu-id="a8e78-116">Action1</span></span> |          | <span data-ttu-id="a8e78-117">Action2</span><span class="sxs-lookup"><span data-stu-id="a8e78-117">Action2</span></span>    | <span data-ttu-id="a8e78-118">0</span><span class="sxs-lookup"><span data-stu-id="a8e78-118">0</span></span>     |           |
| <span data-ttu-id="a8e78-119">Action2</span><span class="sxs-lookup"><span data-stu-id="a8e78-119">Action2</span></span> |          | <span data-ttu-id="a8e78-120">Action1</span><span class="sxs-lookup"><span data-stu-id="a8e78-120">Action1</span></span>    | <span data-ttu-id="a8e78-121">0</span><span class="sxs-lookup"><span data-stu-id="a8e78-121">0</span></span>     |           |



 

<span data-ttu-id="a8e78-122">ICEM03 Invia errori per queste due azioni perché fanno riferimento l'uno all'altro come azioni di base nella tabella ModuleInstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="a8e78-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="a8e78-123">Tutte le azioni nelle tabelle [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)e [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) devono essere azioni di base o derivare la posizione dalla combinazione di un'altra azione e un flag before e After.</span><span class="sxs-lookup"><span data-stu-id="a8e78-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="a8e78-124">Per correggere l'errore, determinare le azioni di base per le due azioni.</span><span class="sxs-lookup"><span data-stu-id="a8e78-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="a8e78-125">Aggiungere un record per le azioni di base con un numero di sequenza predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8e78-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="a8e78-126">Per action1 e Action2 immettere i nomi delle azioni di base nella colonna BaseAction e 0 o 1 nella colonna after.</span><span class="sxs-lookup"><span data-stu-id="a8e78-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8e78-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8e78-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8e78-128">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="a8e78-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



