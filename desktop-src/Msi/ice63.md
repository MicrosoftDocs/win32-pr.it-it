---
description: ICE63 controlla la sequenziazione corretta dell'azione RemoveExistingProducts.
ms.assetid: 4dd67bb0-c08a-4a44-b687-0394a3afc2c4
title: ICE63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5faa6f2ddbcb95cdf12966c2887fe9438a5d610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883362"
---
# <a name="ice63"></a><span data-ttu-id="5c6da-103">ICE63</span><span class="sxs-lookup"><span data-stu-id="5c6da-103">ICE63</span></span>

<span data-ttu-id="5c6da-104">ICE63 controlla la sequenziazione corretta dell' [azione RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="5c6da-104">ICE63 checks for proper sequencing of the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="5c6da-105">È possibile inserire l'azione RemoveExistingProducts:</span><span class="sxs-lookup"><span data-stu-id="5c6da-105">The RemoveExistingProducts action may be placed:</span></span>

1.  <span data-ttu-id="5c6da-106">Tra InstallValidate e InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="5c6da-106">Between InstallValidate and InstallInitialize</span></span>
2.  <span data-ttu-id="5c6da-107">Subito dopo InstallInitialize o dopo InstallInitialize se le azioni tra InstallInitialize e RemoveExistingProducts non generano azioni script.</span><span class="sxs-lookup"><span data-stu-id="5c6da-107">Immediately after InstallInitialize, or after InstallInitialize if the actions between InstallInitialize and RemoveExistingProducts do not generate any script actions.</span></span>
3.  <span data-ttu-id="5c6da-108">Subito dopo InstallExecute o InstallExecuteAgain e prima di InstallFinalize (si applica la stessa restrizione precedente).</span><span class="sxs-lookup"><span data-stu-id="5c6da-108">Immediately after InstallExecute or InstallExecuteAgain and before InstallFinalize (the same restriction as above applies).</span></span>
4.  <span data-ttu-id="5c6da-109">Dopo InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="5c6da-109">After InstallFinalize.</span></span>

<span data-ttu-id="5c6da-110">La mancata correzione di un avviso o di un errore segnalato da ICE63 comporta un errore durante l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5c6da-110">Failure to fix a warning or error reported by ICE63 leads to failure of the upgrade.</span></span>

## <a name="result"></a><span data-ttu-id="5c6da-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="5c6da-111">Result</span></span>

<span data-ttu-id="5c6da-112">ICE63 Invia un avviso o un errore se la sequenziazione dell'azione RemoveExistingProducts non è corretta.</span><span class="sxs-lookup"><span data-stu-id="5c6da-112">ICE63 posts a warning or error if the sequencing of the RemoveExistingProducts action is not correct.</span></span>

## <a name="example"></a><span data-ttu-id="5c6da-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c6da-113">Example</span></span>

<span data-ttu-id="5c6da-114">ICE63 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="5c6da-114">ICE63 reports the following error for the example shown.</span></span>

``` syntax
WARNING: Some action falls between InstallInitialize and RemoveExistingProducts.
```

<span data-ttu-id="5c6da-115">L'azione ' MyCustomAction ' viene eseguita tra InstallInitialize e RemoveExistingProducts.</span><span class="sxs-lookup"><span data-stu-id="5c6da-115">The action 'MyCustomAction' occurs between InstallInitialize and RemoveExistingProducts.</span></span> <span data-ttu-id="5c6da-116">Se MyCustomAction genera qualsiasi azione nello script, causa problemi nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="5c6da-116">If MyCustomAction generates any actions in the script, this causes problems in the installation.</span></span>

<span data-ttu-id="5c6da-117">Per correggere l'errore, verificare che MyCustomAction non generi azioni script né risequenziare le azioni.</span><span class="sxs-lookup"><span data-stu-id="5c6da-117">To fix this error, verify that MyCustomAction does not generate any script actions or resequence the actions.</span></span>

[<span data-ttu-id="5c6da-118">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="5c6da-118">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="5c6da-119">Azione</span><span class="sxs-lookup"><span data-stu-id="5c6da-119">Action</span></span>                 | <span data-ttu-id="5c6da-120">Condizione</span><span class="sxs-lookup"><span data-stu-id="5c6da-120">Condition</span></span> | <span data-ttu-id="5c6da-121">Sequenza</span><span class="sxs-lookup"><span data-stu-id="5c6da-121">Sequence</span></span> |
|------------------------|-----------|----------|
| <span data-ttu-id="5c6da-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="5c6da-122">InstallInitialize</span></span>      |           | <span data-ttu-id="5c6da-123">1000</span><span class="sxs-lookup"><span data-stu-id="5c6da-123">1000</span></span>     |
| <span data-ttu-id="5c6da-124">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="5c6da-124">MyCustomAction</span></span>         |           | <span data-ttu-id="5c6da-125">1010</span><span class="sxs-lookup"><span data-stu-id="5c6da-125">1010</span></span>     |
| <span data-ttu-id="5c6da-126">RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="5c6da-126">RemoveExistingProducts</span></span> |           | <span data-ttu-id="5c6da-127">1020</span><span class="sxs-lookup"><span data-stu-id="5c6da-127">1020</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="5c6da-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c6da-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c6da-129">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="5c6da-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



