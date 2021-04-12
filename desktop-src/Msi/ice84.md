---
description: ICE84 controlla la tabella AdvtExecuteSequence, la tabella AdminExecuteSequence e la tabella InstallExecuteSequence per verificare che le azioni standard seguenti non siano state impostate con le condizioni nel campo condizione.
ms.assetid: 0d1bbf4b-ffab-409e-a292-891dfa823433
title: ICE84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8960f53f5a01e9bec95a02bb3241487aa31aaae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347776"
---
# <a name="ice84"></a><span data-ttu-id="4114d-103">ICE84</span><span class="sxs-lookup"><span data-stu-id="4114d-103">ICE84</span></span>

<span data-ttu-id="4114d-104">ICE84 controlla la tabella [AdvtExecuteSequence](advtexecutesequence-table.md), la [tabella AdminExecuteSequence](adminexecutesequence-table.md)e la [tabella InstallExecuteSequence](installexecutesequence-table.md) per verificare che le [azioni standard](standard-actions.md) seguenti non siano state impostate con le condizioni nel campo condizione.</span><span class="sxs-lookup"><span data-stu-id="4114d-104">ICE84 checks the [AdvtExecuteSequence table](advtexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), and the [InstallExecuteSequence table](installexecutesequence-table.md) to verify that the following [standard actions](standard-actions.md) have not been set with conditions in the Condition field.</span></span>

-   [<span data-ttu-id="4114d-105">Azione CostInitialize</span><span class="sxs-lookup"><span data-stu-id="4114d-105">CostInitialize action</span></span>](costinitialize-action.md)
-   [<span data-ttu-id="4114d-106">Azione CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="4114d-106">CostFinalize action</span></span>](costfinalize-action.md)
-   [<span data-ttu-id="4114d-107">Azione filecost</span><span class="sxs-lookup"><span data-stu-id="4114d-107">FileCost action</span></span>](filecost-action.md)
-   [<span data-ttu-id="4114d-108">Azione InstallValidate</span><span class="sxs-lookup"><span data-stu-id="4114d-108">InstallValidate action</span></span>](installvalidate-action.md)
-   [<span data-ttu-id="4114d-109">Azione InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="4114d-109">InstallInitialize action</span></span>](installinitialize-action.md)
-   [<span data-ttu-id="4114d-110">Azione InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="4114d-110">InstallFinalize action</span></span>](installfinalize-action.md)
-   [<span data-ttu-id="4114d-111">Azione ProcessComponents</span><span class="sxs-lookup"><span data-stu-id="4114d-111">ProcessComponents action</span></span>](processcomponents-action.md)
-   [<span data-ttu-id="4114d-112">Azione PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="4114d-112">PublishFeatures action</span></span>](publishfeatures-action.md)
-   [<span data-ttu-id="4114d-113">Azione PublishProduct</span><span class="sxs-lookup"><span data-stu-id="4114d-113">PublishProduct action</span></span>](publishproduct-action.md)
-   [<span data-ttu-id="4114d-114">Azione RegisterProduct</span><span class="sxs-lookup"><span data-stu-id="4114d-114">RegisterProduct action</span></span>](registerproduct-action.md)
-   [<span data-ttu-id="4114d-115">Azione UnpublishFeatures</span><span class="sxs-lookup"><span data-stu-id="4114d-115">UnpublishFeatures action</span></span>](unpublishfeatures-action.md)

<span data-ttu-id="4114d-116">Se vengono rilevate condizioni, ICE84 pubblica un avviso.</span><span class="sxs-lookup"><span data-stu-id="4114d-116">If conditions are found, ICE84 posts a warning.</span></span>

## <a name="result"></a><span data-ttu-id="4114d-117">Risultato</span><span class="sxs-lookup"><span data-stu-id="4114d-117">Result</span></span>

<span data-ttu-id="4114d-118">ICE84 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="4114d-118">ICE84 posts the following warning.</span></span>



| <span data-ttu-id="4114d-119">Errore ICE84</span><span class="sxs-lookup"><span data-stu-id="4114d-119">ICE84 error</span></span>                                                             | <span data-ttu-id="4114d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4114d-120">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="4114d-121">L'azione ' \[ 1 \] ' trovata nella tabella% s è un'azione obbligatoria con una condizione.</span><span class="sxs-lookup"><span data-stu-id="4114d-121">Action '\[1\]' found in %s table is a required action with a condition.</span></span> | <span data-ttu-id="4114d-122">È stata creata un'azione obbligatoria con una condizione.</span><span class="sxs-lookup"><span data-stu-id="4114d-122">A required action has been authored with a condition.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4114d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4114d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4114d-124">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="4114d-124">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



