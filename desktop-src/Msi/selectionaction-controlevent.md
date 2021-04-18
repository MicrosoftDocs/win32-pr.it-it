---
description: Il controllo SelectionTree usa questo evento per pubblicare una stringa che descrive l'elemento evidenziato. La stringa è uno dei &\# 0034; SEL \* & \# 0034; stringhe della tabella UIText. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: ControlEvent SelectionAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319432"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="ab249-105">ControlEvent SelectionAction</span><span class="sxs-lookup"><span data-stu-id="ab249-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="ab249-106">Il [controllo SelectionTree](selectiontree-control.md) usa questo evento per pubblicare una stringa che descrive l'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="ab249-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="ab249-107">La stringa è una delle stringhe "SEL \* " della [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab249-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="ab249-108">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab249-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ab249-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ab249-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ab249-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ab249-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ab249-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ab249-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ab249-112">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="ab249-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="ab249-113">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="ab249-113">Published By</span></span>

[<span data-ttu-id="ab249-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="ab249-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="ab249-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="ab249-115">Argument</span></span>

<span data-ttu-id="ab249-116">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ab249-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ab249-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="ab249-117">Action on Subscribers</span></span>

<span data-ttu-id="ab249-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="ab249-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ab249-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="ab249-119">Typical Use</span></span>

<span data-ttu-id="ab249-120">Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere questo evento tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab249-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="ab249-121">Il controllo testo Visualizza la spiegazione dell'elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="ab249-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



