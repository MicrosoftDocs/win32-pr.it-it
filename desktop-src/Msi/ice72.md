---
description: ICE72 verifica che le azioni personalizzate non predefinite non vengano utilizzate nella tabella AdvtExecuteSequence.
ms.assetid: b04227d5-5bd6-434a-860c-498d787a1f0a
title: ICE72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d8e1859ffd8123cc7aa3dc801c5484d28ccb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316752"
---
# <a name="ice72"></a><span data-ttu-id="24dc4-103">ICE72</span><span class="sxs-lookup"><span data-stu-id="24dc4-103">ICE72</span></span>

<span data-ttu-id="24dc4-104">ICE72 verifica che le azioni personalizzate non predefinite non vengano utilizzate nella [tabella AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="24dc4-104">ICE72 verifies that non-built-in custom actions are not used in the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span> <span data-ttu-id="24dc4-105">In particolare, nella tabella AdvtExecuteSequence sono consentite solo le azioni personalizzate di tipo 19, tipo 35 e tipo 51.</span><span class="sxs-lookup"><span data-stu-id="24dc4-105">Specifically, only type 19, type 35, and type 51 custom actions are allowed in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="24dc4-106">Se vengono utilizzate altre azioni personalizzate, l'annuncio potrebbe non comportarsi come previsto.</span><span class="sxs-lookup"><span data-stu-id="24dc4-106">If other custom actions are used, advertisement may not behave as expected.</span></span>

## <a name="result"></a><span data-ttu-id="24dc4-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="24dc4-107">Result</span></span>

<span data-ttu-id="24dc4-108">ICE72 restituisce un errore se la tabella AdvExecuteSequence utilizza azioni personalizzate diverse da tipo 35, tipo 51 e tipo 19.</span><span class="sxs-lookup"><span data-stu-id="24dc4-108">ICE72 returns an error if the AdvExecuteSequence table uses custom actions other than type 35, type 51, and type 19.</span></span>

## <a name="example"></a><span data-ttu-id="24dc4-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="24dc4-109">Example</span></span>

<span data-ttu-id="24dc4-110">ICE72 segnala l'errore seguente per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="24dc4-110">ICE72 reports the following error for the example shown:</span></span>

``` syntax
Custom Action 'CA1' in the AdvtExecuteSequence table is not allowed. Only built-in custom actions are allowed.
```

<span data-ttu-id="24dc4-111">Per correggere l'errore, rimuovere "CA1" dalla tabella AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="24dc4-111">To fix the error, remove 'CA1' from the AdvtExecuteSequence table.</span></span>

<span data-ttu-id="24dc4-112">[Tabella AdvtExecuteSequence](advtexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24dc4-112">[AdvtExecuteSequence Table](advtexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="24dc4-113">Azione</span><span class="sxs-lookup"><span data-stu-id="24dc4-113">Action</span></span> |
|--------|
| <span data-ttu-id="24dc4-114">CA1</span><span class="sxs-lookup"><span data-stu-id="24dc4-114">CA1</span></span>    |
| <span data-ttu-id="24dc4-115">CA35</span><span class="sxs-lookup"><span data-stu-id="24dc4-115">CA35</span></span>   |



 

<span data-ttu-id="24dc4-116">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24dc4-116">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="24dc4-117">Azione</span><span class="sxs-lookup"><span data-stu-id="24dc4-117">Action</span></span> | <span data-ttu-id="24dc4-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="24dc4-118">Type</span></span> |
|--------|------|
| <span data-ttu-id="24dc4-119">CA1</span><span class="sxs-lookup"><span data-stu-id="24dc4-119">CA1</span></span>    | <span data-ttu-id="24dc4-120">1</span><span class="sxs-lookup"><span data-stu-id="24dc4-120">1</span></span>    |
| <span data-ttu-id="24dc4-121">CA35</span><span class="sxs-lookup"><span data-stu-id="24dc4-121">CA35</span></span>   | <span data-ttu-id="24dc4-122">35</span><span class="sxs-lookup"><span data-stu-id="24dc4-122">35</span></span>   |



 

## <a name="tables-used-during-execution"></a><span data-ttu-id="24dc4-123">Tabelle utilizzate durante l'esecuzione</span><span class="sxs-lookup"><span data-stu-id="24dc4-123">Tables used during execution</span></span>

[<span data-ttu-id="24dc4-124">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="24dc4-124">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)

[<span data-ttu-id="24dc4-125">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="24dc4-125">CustomAction Table</span></span>](customaction-table.md)

## <a name="related-topics"></a><span data-ttu-id="24dc4-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24dc4-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24dc4-127">Tipo di azione personalizzata 19</span><span class="sxs-lookup"><span data-stu-id="24dc4-127">Custom Action Type 19</span></span>](custom-action-type-19.md)
</dt> <dt>

[<span data-ttu-id="24dc4-128">Tipo di azione personalizzata 35</span><span class="sxs-lookup"><span data-stu-id="24dc4-128">Custom Action Type 35</span></span>](custom-action-type-35.md)
</dt> <dt>

[<span data-ttu-id="24dc4-129">Tipo di azione personalizzata 51</span><span class="sxs-lookup"><span data-stu-id="24dc4-129">Custom Action Type 51</span></span>](custom-action-type-51.md)
</dt> <dt>

[<span data-ttu-id="24dc4-130">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="24dc4-130">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



