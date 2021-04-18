---
description: Il controllo SelectionTree usa l'evento SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che diventano inutili. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: ControlEvent SelectionNoItems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319431"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="22aa3-104">ControlEvent SelectionNoItems</span><span class="sxs-lookup"><span data-stu-id="22aa3-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="22aa3-105">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che diventano inutili.</span><span class="sxs-lookup"><span data-stu-id="22aa3-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="22aa3-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="22aa3-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="22aa3-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="22aa3-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="22aa3-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="22aa3-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="22aa3-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="22aa3-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="22aa3-110">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="22aa3-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="22aa3-111">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="22aa3-111">Published By</span></span>

<span data-ttu-id="22aa3-112">[SelectionTree controllare](selectiontree-control.md) se la selezione non include nodi.</span><span class="sxs-lookup"><span data-stu-id="22aa3-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="22aa3-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="22aa3-113">Argument</span></span>

<span data-ttu-id="22aa3-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="22aa3-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="22aa3-115">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="22aa3-115">Action on Subscribers</span></span>

<span data-ttu-id="22aa3-116">Elimina il testo della descrizione dell'elemento obsoleto o Disabilita i pulsanti obsoleti.</span><span class="sxs-lookup"><span data-stu-id="22aa3-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="22aa3-117">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="22aa3-117">Typical Use</span></span>

<span data-ttu-id="22aa3-118">Può essere usato per disabilitare i pulsanti Next, reset e DiskCost della finestra di [dialogo di selezione](selection-dialog.md) quando una selezione non contiene nodi e questi pulsanti diventano inutili.</span><span class="sxs-lookup"><span data-stu-id="22aa3-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



