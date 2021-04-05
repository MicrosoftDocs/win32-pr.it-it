---
description: ICE82 verifica che l'azione RegisterProduct, l'azione RegisterUser, l'azione PublishProduct e l'azione PublishFeatures siano presenti nella tabella InstallExecuteSequence. Il pacchetto viene convalidato se sono presenti tutte le azioni.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758414"
---
# <a name="ice82"></a><span data-ttu-id="60a75-104">ICE82</span><span class="sxs-lookup"><span data-stu-id="60a75-104">ICE82</span></span>

<span data-ttu-id="60a75-105">ICE82 verifica che l'azione [RegisterProduct](registerproduct-action.md), l'azione [RegisterUser](registeruser-action.md), l'azione [PublishProduct](publishproduct-action.md)e l' [azione PublishFeatures](publishfeatures-action.md) siano presenti nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="60a75-105">ICE82 validates that the [RegisterProduct Action](registerproduct-action.md), [RegisterUser Action](registeruser-action.md), [PublishProduct Action](publishproduct-action.md), and [PublishFeatures Action](publishfeatures-action.md) are all present in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="60a75-106">Il pacchetto viene convalidato se sono presenti tutte le azioni.</span><span class="sxs-lookup"><span data-stu-id="60a75-106">The package is validated if all the actions are present.</span></span>

<span data-ttu-id="60a75-107">ICE82 pubblica un avviso se sono presenti due azioni con lo stesso numero di sequenza elencato nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="60a75-107">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables .</span></span>

## <a name="result"></a><span data-ttu-id="60a75-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="60a75-108">Result</span></span>

<span data-ttu-id="60a75-109">ICE82 invia gli avvisi seguenti.</span><span class="sxs-lookup"><span data-stu-id="60a75-109">ICE82 posts the following warnings.</span></span>



| <span data-ttu-id="60a75-110">Avviso di ICE82</span><span class="sxs-lookup"><span data-stu-id="60a75-110">ICE82 warning</span></span>                                                                                                                                                                                                                 | <span data-ttu-id="60a75-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a75-111">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60a75-112">La tabella InstallExecuteSequence non contiene il set di azioni indicato di seguito: azioni mancanti:</span><span class="sxs-lookup"><span data-stu-id="60a75-112">The InstallExecuteSequence table does not contain the set of actions mentioned below: Actions Missing:</span></span><br/> <span data-ttu-id="60a75-113">Funzionalità di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="60a75-113">Publish Features</span></span><br/> <span data-ttu-id="60a75-114">Pubblica prodotto</span><span class="sxs-lookup"><span data-stu-id="60a75-114">Publish Product</span></span><br/> <span data-ttu-id="60a75-115">Registrare il prodotto</span><span class="sxs-lookup"><span data-stu-id="60a75-115">Register Product</span></span><br/> <span data-ttu-id="60a75-116">Registra utente</span><span class="sxs-lookup"><span data-stu-id="60a75-116">Register User</span></span><br/> | <span data-ttu-id="60a75-117">L'azione personalizzata ICE82 Invia un avviso se tutte e quattro le azioni sono assenti.</span><span class="sxs-lookup"><span data-stu-id="60a75-117">ICE82 custom action posts a warning if all four actions are absent.</span></span>                                                                                                                                         |
| <span data-ttu-id="60a75-118">Questa azione \[ 1 \] presenta il numero di sequenza 2 duplicato \[ \] nella tabella \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="60a75-118">This action \[1\] has duplicate sequence number \[2\] in the table \[3\].</span></span>                                                                                                                                                     | <span data-ttu-id="60a75-119">ICE82 pubblica un avviso se sono presenti due azioni con lo stesso numero di sequenza elencato nelle tabelle InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence o AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="60a75-119">ICE82 posts a warning if there are two actions with the same sequence number listed in the InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence, or AdvtExecuteSequence tables.</span></span> |



 

<span data-ttu-id="60a75-120">ICE82 invia i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="60a75-120">ICE82 posts the following errors.</span></span>



| <span data-ttu-id="60a75-121">Errore ICE82</span><span class="sxs-lookup"><span data-stu-id="60a75-121">ICE82 error</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="60a75-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60a75-122">Description</span></span>                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="60a75-123">InstallExecuteSequence deve contenere tutte le azioni indicate di seguito oppure nessuna delle azioni presenti</span><span class="sxs-lookup"><span data-stu-id="60a75-123">The InstallExecuteSequence should either contain all of the actions mentioned below or none of them Actions Present</span></span><br/> <List of actions present> <br/> <span data-ttu-id="60a75-124">Azioni mancanti:</span><span class="sxs-lookup"><span data-stu-id="60a75-124">Actions Missing:</span></span><br/> <List of actions missing> <br/> | <span data-ttu-id="60a75-125">ICE82 Invia un errore se alcune delle quattro azioni sono presenti e altre sono assenti.</span><span class="sxs-lookup"><span data-stu-id="60a75-125">ICE82 posts an error if some of the four actions are present and others are absent.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="60a75-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60a75-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60a75-127">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="60a75-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




