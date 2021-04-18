---
description: L'azione CostInitialize avvia il processo di determinazione dei costi di installazione.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Azione CostInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313815"
---
# <a name="costinitialize-action"></a><span data-ttu-id="9d213-103">Azione CostInitialize</span><span class="sxs-lookup"><span data-stu-id="9d213-103">CostInitialize Action</span></span>

<span data-ttu-id="9d213-104">L'azione CostInitialize avvia il processo di [*determinazione dei costi*](c-gly.md) di installazione.</span><span class="sxs-lookup"><span data-stu-id="9d213-104">The CostInitialize action initiates the installation [*costing*](c-gly.md) process.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9d213-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="9d213-105">Sequence Restrictions</span></span>

<span data-ttu-id="9d213-106">Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="9d213-106">Any standard or [custom](custom-actions.md) actions that affect costing should be sequenced before the CostInitialize action.</span></span> <span data-ttu-id="9d213-107">Chiamare l'azione [filecost](filecost-action.md) immediatamente dopo l'azione CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="9d213-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action.</span></span> <span data-ttu-id="9d213-108">Chiamare quindi l'azione [CostFinalize secondo](costfinalize-action.md) dopo l'azione CostInitialize azione per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9d213-108">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9d213-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="9d213-109">ActionData Messages</span></span>

<span data-ttu-id="9d213-110">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="9d213-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d213-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9d213-111">Remarks</span></span>

<span data-ttu-id="9d213-112">L'azione CostInitialize carica la tabella dei componenti e la tabella delle [funzionalità](feature-table.md) in memoria.</span><span class="sxs-lookup"><span data-stu-id="9d213-112">The CostInitialize action loads the Component table and [Feature](feature-table.md) table into memory.</span></span>

<span data-ttu-id="9d213-113">Per ulteriori informazioni sul processo di [*determinazione dei costi*](c-gly.md) nel programma di installazione, vedere [Costing di file](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="9d213-113">For more information on the [*costing*](c-gly.md) process in the installer, see [File Costing](file-costing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d213-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9d213-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d213-115">Costo file</span><span class="sxs-lookup"><span data-stu-id="9d213-115">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



