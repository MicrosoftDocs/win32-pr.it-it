---
description: FileCostaction avvia le azioni di installazione standard di costingof dinamica.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Azione filecost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058387"
---
# <a name="filecost-action"></a><span data-ttu-id="c8876-103">Azione filecost</span><span class="sxs-lookup"><span data-stu-id="c8876-103">FileCost Action</span></span>

<span data-ttu-id="c8876-104">Il FileCostaction avvia il [*costo*](c-gly.md)dinamico delle azioni di installazione standard.</span><span class="sxs-lookup"><span data-stu-id="c8876-104">The FileCostaction initiates dynamic [*costing*](c-gly.md)of standard installation actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c8876-105">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="c8876-105">ActionData Messages</span></span>

<span data-ttu-id="c8876-106">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="c8876-106">There are no ActionData messages.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c8876-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="c8876-107">Sequence Restrictions</span></span>

<span data-ttu-id="c8876-108">Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c8876-108">Any standard or [custom actions](custom-actions.md) that affect costing should sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="c8876-109">Chiamare l'azione filecost immediatamente dopo l'azione CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="c8876-109">Call the FileCost action immediately following the CostInitialize action.</span></span> <span data-ttu-id="c8876-110">Chiamare quindi l'azione [CostFinalize secondo](costfinalize-action.md) dopo l'azione CostInitialize per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c8876-110">Then call the [CostFinalize](costfinalize-action.md) action following the CostInitialize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="c8876-111">L'azione [CostInitialize](costinitialize-action.md) deve essere eseguita prima dell'azione filecost.</span><span class="sxs-lookup"><span data-stu-id="c8876-111">The [CostInitialize](costinitialize-action.md) action must be executed before the FileCost action.</span></span> <span data-ttu-id="c8876-112">Il programma di installazione determina quindi il costo dello spazio su disco di ogni file nella tabella dei [file](file-table.md) , in base ai singoli componenti (vedere la [tabella dei componenti](component-table.md)), accettando sia il clustering del [*volume*](v-gly.md) che la presenza di file esistenti che potrebbero dover essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="c8876-112">The installer then determines the disk-space cost of every file in the [File](file-table.md) table, on a per-component basis (See [Component Table](component-table.md)), taking both [*volume*](v-gly.md) clustering and the presence of existing files that may need to be overwritten into account.</span></span> <span data-ttu-id="c8876-113">Verranno considerate anche tutte le azioni che utilizzano o rilasciano spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="c8876-113">All actions that consume or release disk space are also considered.</span></span> <span data-ttu-id="c8876-114">Se viene trovato un file esistente, viene eseguito un controllo della versione del file per determinare se è effettivamente necessario installare il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="c8876-114">If an existing file is found, a file version check is performed to determine whether the new file actually needs to be installed or not.</span></span> <span data-ttu-id="c8876-115">Se il numero di versione del file esistente è uguale o maggiore, il file esistente non viene sovrascritto e non è stato eseguito alcun costo dello spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="c8876-115">If the existing file is of an equal or greater version number, the existing file is not overwritten and no disk-space cost is incurred.</span></span> <span data-ttu-id="c8876-116">In tutti i casi, il programma di installazione utilizza i risultati del controllo del numero di versione per impostare lo stato di installazione di ogni file.</span><span class="sxs-lookup"><span data-stu-id="c8876-116">In all cases, the installer uses the results of version number checking to set the installation state of each file.</span></span>

<span data-ttu-id="c8876-117">L'azione filecost Inizializza il calcolo dei costi con TheInstaller.</span><span class="sxs-lookup"><span data-stu-id="c8876-117">The FileCost action initializes cost calculation with theinstaller.</span></span> <span data-ttu-id="c8876-118">Il [*costo*](c-gly.md) dinamico effettivo non si verifica finché non viene eseguita l'azione [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c8876-118">Actual dynamic [*costing*](c-gly.md) does not occur until the [CostFinalize](costfinalize-action.md) action is executed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8876-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8876-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8876-120">Costo file</span><span class="sxs-lookup"><span data-stu-id="c8876-120">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



