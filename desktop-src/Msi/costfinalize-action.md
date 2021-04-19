---
description: L'azione CostFinalize secondo termina il processo di determinazione dei costi di installazione interna iniziato dall'azione CostInitialize.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Azione CostFinalize secondo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317766"
---
# <a name="costfinalize-action"></a><span data-ttu-id="8627b-103">Azione CostFinalize secondo</span><span class="sxs-lookup"><span data-stu-id="8627b-103">CostFinalize Action</span></span>

<span data-ttu-id="8627b-104">L'azione CostFinalize secondo termina il processo di [*determinazione dei costi*](c-gly.md) di installazione interna iniziato dall'azione [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8627b-104">The CostFinalize action ends the internal installation [*costing*](c-gly.md) process begun by the [CostInitialize](costinitialize-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8627b-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="8627b-105">Sequence Restrictions</span></span>

<span data-ttu-id="8627b-106">Tutte le azioni standard o [personalizzate](custom-actions.md) che influiscono sui costi devono essere sequenziate prima dell'azione [CostInitialize](costinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8627b-106">Any standard or [custom actions](custom-actions.md) that affect costing should be sequenced before the [CostInitialize](costinitialize-action.md) action.</span></span> <span data-ttu-id="8627b-107">Chiamare l'azione [filecost](filecost-action.md) immediatamente dopo l'azione CostInitialize, quindi chiamare l'azione CostFinalize secondo per rendere disponibili al programma di installazione tutti i calcoli dei costi finali tramite la tabella [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8627b-107">Call the [FileCost](filecost-action.md) action immediately following the CostInitialize action and then call the CostFinalize action to make all final cost calculations available to the installer through the [Component](component-table.md) table.</span></span>

<span data-ttu-id="8627b-108">È necessario eseguire l'azione CostFinalize secondo prima di avviare qualsiasi sequenza dell'interfaccia utente che consente all'utente di visualizzare o modificare selezioni o directory della tabella delle [funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8627b-108">The CostFinalize action must be executed before starting any user interface sequence which allows the user to view or modify [Feature](feature-table.md) table selections or directories.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8627b-109">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="8627b-109">ActionData Messages</span></span>

<span data-ttu-id="8627b-110">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="8627b-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="8627b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8627b-111">Remarks</span></span>

<span data-ttu-id="8627b-112">L'azione CostFinalize secondo esegue una query sulla tabella [Condition](condition-table.md) per determinare quali funzionalità sono pianificate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8627b-112">The CostFinalize action queries the [Condition](condition-table.md) table to determine which features are scheduled to be installed.</span></span> <span data-ttu-id="8627b-113">Il costo viene eseguito per ogni componente della tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8627b-113">Costing is done for each component in the [Component](component-table.md) table.</span></span>

<span data-ttu-id="8627b-114">L'azione CostFinalize secondo verifica anche che tutte le directory di destinazione siano scrivibili prima di consentire l'installazione per continuare.</span><span class="sxs-lookup"><span data-stu-id="8627b-114">The CostFinalize action also verifies that all the target directories are writable before allowing the installation to continue.</span></span>

> [!Note]  
> <span data-ttu-id="8627b-115">Durante un' [installazione amministrativa](administrative-installation.md), CostFinalize secondo imposta tutte le funzionalità per l'installazione ad eccezione delle funzionalità con 0 create nella colonna livello della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8627b-115">During an [administrative installation](administrative-installation.md), CostFinalize sets all features for installation except features having 0 authored in the Level column of the [Feature table](feature-table.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8627b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8627b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8627b-117">Costo file</span><span class="sxs-lookup"><span data-stu-id="8627b-117">File Costing</span></span>](file-costing.md)
</dt> </dl>

 

 



