---
description: Il controllo SelectionTree usa l'evento SelectionBrowse per generare una finestra di dialogo di esplorazione che consente di modificare il percorso dell'elemento evidenziato.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: ControlEvent SelectionBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350226"
---
# <a name="selectionbrowse-controlevent"></a><span data-ttu-id="beed9-103">ControlEvent SelectionBrowse</span><span class="sxs-lookup"><span data-stu-id="beed9-103">SelectionBrowse ControlEvent</span></span>

<span data-ttu-id="beed9-104">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionBrowse per generare una finestra di dialogo di **esplorazione** che consente di modificare il percorso dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="beed9-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionBrowse event to spawn a **Browse** dialog box making it possible to modify the path of the highlighted item.</span></span>

<span data-ttu-id="beed9-105">Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento.</span><span class="sxs-lookup"><span data-stu-id="beed9-105">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="beed9-106">L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="beed9-106">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="beed9-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="beed9-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="beed9-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="beed9-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="beed9-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="beed9-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="beed9-110">Tutti i controlli che pubblicano un evento SelectionBrowse diventano disabilitati se è stata selezionata una funzionalità già installata, non configurabile o non selezionata per l'installazione locale.</span><span class="sxs-lookup"><span data-stu-id="beed9-110">Any controls that publish a SelectionBrowse event become disabled if a feature has been selected that is already installed, not configurable, or not selected for local installation.</span></span> <span data-ttu-id="beed9-111">Per poter essere configurata, la funzionalità deve avere una [proprietà pubblica](public-properties.md) immessa nel \_ campo Directory della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="beed9-111">To be configurable, the feature must have a [public property](public-properties.md) entered in the Directory\_ field of the [Feature table](feature-table.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="beed9-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="beed9-112">Published By</span></span>

[<span data-ttu-id="beed9-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="beed9-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="beed9-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="beed9-114">Argument</span></span>

<span data-ttu-id="beed9-115">Nome della finestra di dialogo da generare.</span><span class="sxs-lookup"><span data-stu-id="beed9-115">The name of the dialog to be spawned.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="beed9-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="beed9-116">Action on Subscribers</span></span>

<span data-ttu-id="beed9-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="beed9-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="beed9-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="beed9-118">Typical Use</span></span>

<span data-ttu-id="beed9-119">Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale del SelectionTree utilizza questo evento per attivare la finestra di dialogo **Sfoglia** .</span><span class="sxs-lookup"><span data-stu-id="beed9-119">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the SelectionTree uses this event to trigger the **Browse** dialog box.</span></span>

 

 



