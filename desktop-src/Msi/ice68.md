---
description: ICE68 verifica che tutti i tipi di azione personalizzati necessari per un'installazione siano validi.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318667"
---
# <a name="ice68"></a><span data-ttu-id="476d3-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="476d3-103">ICE68</span></span>

<span data-ttu-id="476d3-104">ICE68 verifica che tutti i tipi di azione personalizzati necessari per un'installazione siano validi.</span><span class="sxs-lookup"><span data-stu-id="476d3-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="476d3-105">Se si verifica un errore durante la correzione dell'errore segnalato da ICE68, un'installazione che tenta di eseguire l'azione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="476d3-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="476d3-106">ICE68 genera un avviso se l'attributo **msidbCustomActionTypeNoImpersonate** è impostato senza impostare anche l'attributo **msidbCustomActionTypeInScript** .</span><span class="sxs-lookup"><span data-stu-id="476d3-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="476d3-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="476d3-107">Result</span></span>

<span data-ttu-id="476d3-108">ICE68 restituisce un errore se un tipo di azione necessario per un'installazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="476d3-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="476d3-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="476d3-109">Example</span></span>

<span data-ttu-id="476d3-110">ICE68 invia l'avviso seguente se un'azione personalizzata ha il bit **msidbCustomActionTypeNoImpersonate** impostato nel campo Type della tabella CustomAction senza impostare anche **msidbCustomActionTypeInScript** .</span><span class="sxs-lookup"><span data-stu-id="476d3-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="476d3-111">Per correggere il problema, includere **msidbCustomActionTypeInScript** (0x400) se l'azione personalizzata include **msidbCustomActionTypeNoImpersonate** (0x800).</span><span class="sxs-lookup"><span data-stu-id="476d3-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="476d3-112">In caso contrario, il programma di installazione ignora l'attributo **msidbCustomActionTypeNoImpersonate** .</span><span class="sxs-lookup"><span data-stu-id="476d3-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="476d3-113">Per altre informazioni, vedere [azione personalizzata In-Script opzioni di esecuzione](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="476d3-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="476d3-114">ICE68 segnala l'errore seguente per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="476d3-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="476d3-115">1027 non è un tipo di azione valido.</span><span class="sxs-lookup"><span data-stu-id="476d3-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="476d3-116">Per correggere l'errore, scegliere un tipo di azione personalizzata valido.</span><span class="sxs-lookup"><span data-stu-id="476d3-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="476d3-117">[Tabella CustomAction](customaction-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="476d3-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="476d3-118">Azione</span><span class="sxs-lookup"><span data-stu-id="476d3-118">Action</span></span>  | <span data-ttu-id="476d3-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="476d3-119">Type</span></span> | <span data-ttu-id="476d3-120">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="476d3-120">Source</span></span>   | <span data-ttu-id="476d3-121">Destinazione</span><span class="sxs-lookup"><span data-stu-id="476d3-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="476d3-122">Action1</span><span class="sxs-lookup"><span data-stu-id="476d3-122">Action1</span></span> | <span data-ttu-id="476d3-123">1027</span><span class="sxs-lookup"><span data-stu-id="476d3-123">1027</span></span> | <span data-ttu-id="476d3-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="476d3-124">Argument</span></span> | <span data-ttu-id="476d3-125">Component1</span><span class="sxs-lookup"><span data-stu-id="476d3-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="476d3-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="476d3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="476d3-127">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="476d3-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



