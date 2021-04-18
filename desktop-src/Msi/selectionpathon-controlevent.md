---
description: Il controllo SelectionTree usa l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: ControlEvent SelectionPathOn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319428"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="c769e-104">ControlEvent SelectionPathOn</span><span class="sxs-lookup"><span data-stu-id="c769e-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="c769e-105">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="c769e-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="c769e-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c769e-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c769e-107">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="c769e-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="c769e-108">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c769e-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c769e-109">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c769e-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c769e-110">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c769e-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="c769e-111">Il ControlEvent SelectionPathOn non viene mai pubblicato durante un' [installazione di manutenzione](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c769e-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c769e-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="c769e-112">Published By</span></span>

[<span data-ttu-id="c769e-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="c769e-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="c769e-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="c769e-114">Argument</span></span>

<span data-ttu-id="c769e-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="c769e-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c769e-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="c769e-116">Action on Subscribers</span></span>

<span data-ttu-id="c769e-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="c769e-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c769e-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="c769e-118">Typical Use</span></span>

<span data-ttu-id="c769e-119">Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c769e-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="c769e-120">Il controllo testo Visualizza la didascalia del percorso di selezione.</span><span class="sxs-lookup"><span data-stu-id="c769e-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="c769e-121">Questo controllo testo è visibile o nascosto a seconda dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c769e-121">This text control is visible or hidden depending on the event.</span></span>

 

 



