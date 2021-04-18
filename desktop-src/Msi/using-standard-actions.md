---
description: Un'azione viene eseguita nel Windows Installer chiamando la funzione MsiDoAction o includendo l'azione in una tabella di sequenza.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso di azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309992"
---
# <a name="using-standard-actions"></a><span data-ttu-id="d5494-103">Uso di azioni standard</span><span class="sxs-lookup"><span data-stu-id="d5494-103">Using Standard Actions</span></span>

<span data-ttu-id="d5494-104">Un'azione viene eseguita nel Windows Installer chiamando la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o includendo l'azione in una tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d5494-104">An action is executed in the Windows Installer either by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function or including the action in a sequence table.</span></span> <span data-ttu-id="d5494-105">Poiché la maggior parte delle azioni incapsula un solo scopo, il modo più comune per usare le azioni consiste nell'ordinare una serie di azioni in una sequenza per eseguire un'attività più ampia.</span><span class="sxs-lookup"><span data-stu-id="d5494-105">Because most actions encapsulate a single purpose, the most common way to use actions is to order a series of actions into a sequence to accomplish a larger task.</span></span> <span data-ttu-id="d5494-106">Il programma di installazione prevede tre azioni di livello principale standard che chiamano un set associato di tabelle di sequenza.</span><span class="sxs-lookup"><span data-stu-id="d5494-106">The installer has three standard top-level actions that call an associated set of sequence tables.</span></span> <span data-ttu-id="d5494-107">Queste tabelle di sequenza associate possono contenere azioni standard, azioni personalizzate ed elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d5494-107">These associated sequence tables may contain standard actions, custom actions, and user-interface elements.</span></span> <span data-ttu-id="d5494-108">A ogni azione in una tabella di sequenza è associato un numero di sequenza e può inoltre essere associata un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="d5494-108">Each action in a sequence table has an associated sequence number and may also have an associated conditional expression.</span></span> <span data-ttu-id="d5494-109">Tutte le azioni in una tabella di sequenza vengono visitate in ordine e vengono eseguite solo se l'espressione condizionale restituisce true.</span><span class="sxs-lookup"><span data-stu-id="d5494-109">All actions in a sequence table are visited in order and are only executed if the conditional expression evaluates to True.</span></span>

<span data-ttu-id="d5494-110">Mentre un'azione standard può avere un numero di sequenza associato, molti presentano restrizioni di sequenza che devono essere seguite per il corretto funzionamento dell'azione.</span><span class="sxs-lookup"><span data-stu-id="d5494-110">While a standard action can have any sequence number associated with it, many have sequence restrictions which must be followed for the action to function properly.</span></span> <span data-ttu-id="d5494-111">Ad esempio, l' [azione filecost](filecost-action.md)deve essere chiamata dopo l' [azione CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d5494-111">For example the [FileCost action](filecost-action.md), must be called after the [CostInitialize action](costinitialize-action.md).</span></span> <span data-ttu-id="d5494-112">Per ulteriori informazioni sulle restrizioni di sequenziazione delle azioni standard, vedere [azioni con restrizioni di sequenziazione](actions-with-sequencing-restrictions.md), [azioni senza restrizioni di sequenziazione](actions-without-sequencing-restrictions.md)o [riferimento a azioni standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d5494-112">For more information on standard action sequencing restrictions, see [Actions with Sequencing Restrictions](actions-with-sequencing-restrictions.md), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md), or [Standard Actions Reference](standard-actions-reference.md).</span></span>

<span data-ttu-id="d5494-113">Negli argomenti seguenti vengono fornite ulteriori informazioni sull'utilizzo delle azioni standard.</span><span class="sxs-lookup"><span data-stu-id="d5494-113">The following topics provide more information about using standard actions.</span></span>

-   [<span data-ttu-id="d5494-114">Pubblicazione di prodotti, funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="d5494-114">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)
-   [<span data-ttu-id="d5494-115">Ricerca file</span><span class="sxs-lookup"><span data-stu-id="d5494-115">File Searching</span></span>](file-searching.md)
-   [<span data-ttu-id="d5494-116">Costo file</span><span class="sxs-lookup"><span data-stu-id="d5494-116">File Costing</span></span>](file-costing.md)
-   [<span data-ttu-id="d5494-117">Installazione file</span><span class="sxs-lookup"><span data-stu-id="d5494-117">File Installation</span></span>](file-installation.md)
-   [<span data-ttu-id="d5494-118">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d5494-118">Modifying the Registry</span></span>](modifying-the-registry.md)
-   [<span data-ttu-id="d5494-119">Azioni in esecuzione</span><span class="sxs-lookup"><span data-stu-id="d5494-119">Running Actions</span></span>](running-actions.md)

<span data-ttu-id="d5494-120">Vedere anche le [informazioni di riferimento sulle azioni standard o sulle](about-standard-actions.md) [azioni standard](standard-actions-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d5494-120">See also [About Standard Actions](about-standard-actions.md) or [Standard Actions Reference](standard-actions-reference.md).</span></span>

 

 



