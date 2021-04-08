---
description: Il controllo SelectionTree usa l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: ControlEvent SelectionPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967677"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="614a5-103">ControlEvent SelectionPath</span><span class="sxs-lookup"><span data-stu-id="614a5-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="614a5-104">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="614a5-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="614a5-105">Se l'elemento è selezionato per l'esecuzione dall'origine, questo è il percorso dell'origine.</span><span class="sxs-lookup"><span data-stu-id="614a5-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="614a5-106">Se l'elemento è selezionato come assente, la stringa è la stringa **AbsentPath** dalla [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="614a5-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="614a5-107">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="614a5-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="614a5-108">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="614a5-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="614a5-109">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="614a5-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="614a5-110">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="614a5-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="614a5-111">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="614a5-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="614a5-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="614a5-112">Published By</span></span>

[<span data-ttu-id="614a5-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="614a5-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="614a5-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="614a5-114">Argument</span></span>

<span data-ttu-id="614a5-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="614a5-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="614a5-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="614a5-116">Action on Subscribers</span></span>

<span data-ttu-id="614a5-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="614a5-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="614a5-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="614a5-118">Typical Use</span></span>

<span data-ttu-id="614a5-119">Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="614a5-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="614a5-120">Il controllo testo Visualizza il percorso dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="614a5-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



