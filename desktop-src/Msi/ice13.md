---
description: ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle AdminUISequence o InstallUISequence. Le finestre di dialogo non devono essere elencate nelle tabelle InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967792"
---
# <a name="ice13"></a><span data-ttu-id="87c91-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="87c91-104">ICE13</span></span>

<span data-ttu-id="87c91-105">ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle [AdminUISequence](adminuisequence-table.md)o [InstallUISequence](installuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="87c91-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="87c91-106">Le finestre di dialogo non devono essere elencate nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="87c91-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="87c91-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="87c91-107">Result</span></span>

<span data-ttu-id="87c91-108">ICE13 Invia un messaggio di errore se viene visualizzata una finestra di dialogo in una tabella di sequenza di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87c91-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="87c91-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="87c91-109">Example</span></span>

<span data-ttu-id="87c91-110">Per l'esempio seguente, ICE13 Invia un messaggio di errore che informa che non è possibile elencare ' WelcomeDialog ' nella tabella ' InstallExecuteSequence '.</span><span class="sxs-lookup"><span data-stu-id="87c91-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="87c91-111">[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="87c91-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="87c91-112">Azione</span><span class="sxs-lookup"><span data-stu-id="87c91-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="87c91-113">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="87c91-113">InstallFinalize</span></span> |
| <span data-ttu-id="87c91-114">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="87c91-114">CostFinalize</span></span>    |
| <span data-ttu-id="87c91-115">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="87c91-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="87c91-116">[Tabella InstallUISequence](installuisequence-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="87c91-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="87c91-117">Azione</span><span class="sxs-lookup"><span data-stu-id="87c91-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="87c91-118">CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="87c91-118">CostFinalize</span></span>   |
| <span data-ttu-id="87c91-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="87c91-119">CostInitialize</span></span> |
| <span data-ttu-id="87c91-120">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="87c91-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="87c91-121">[Tabella finestra di dialogo](dialog-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="87c91-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="87c91-122">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="87c91-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="87c91-123">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="87c91-123">BrowseDialog</span></span>  |
| <span data-ttu-id="87c91-124">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="87c91-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="87c91-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87c91-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87c91-126">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="87c91-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



