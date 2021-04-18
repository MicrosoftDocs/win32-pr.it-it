---
description: Il programma di installazione utilizza questo evento per visualizzare una stringa informativa durante la compilazione dello script di esecuzione dell'installazione.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ControlEvent ScriptInProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312317"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="e0069-103">ControlEvent ScriptInProgress</span><span class="sxs-lookup"><span data-stu-id="e0069-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="e0069-104">Il programma di installazione utilizza questo evento per visualizzare una stringa informativa durante la compilazione dello script di esecuzione dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="e0069-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="e0069-105">La stringa informativa può essere visualizzata in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="e0069-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="e0069-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0069-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="e0069-107">Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e0069-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="e0069-108">Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="e0069-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="e0069-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="e0069-109">Published By</span></span>

<span data-ttu-id="e0069-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="e0069-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="e0069-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="e0069-111">Argument</span></span>

<span data-ttu-id="e0069-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e0069-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="e0069-113">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="e0069-113">Action on Subscribers</span></span>

<span data-ttu-id="e0069-114">Un [controllo di testo](text-control.md) che sottoscrive ScriptInProgress visualizzerà la stringa di testo specificata nella [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0069-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="e0069-115">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="e0069-115">Typical Use</span></span>

<span data-ttu-id="e0069-116">Durante la compilazione dello script di esecuzione, il programma di installazione visualizza una ProgressBar che indica il tempo rimanente prima dell'inizio dell'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="e0069-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="e0069-117">Al momento, l'autore del pacchetto può visualizzare un messaggio preliminare che illustra il ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="e0069-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="e0069-118">Per visualizzare un messaggio preliminare, includere un [controllo di testo](text-control.md) nella stessa finestra di dialogo non modale della ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="e0069-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="e0069-119">Consente di specificare che questo controllo di testo sottoscrive il ControlEvent ScriptInProgress tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="e0069-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="e0069-120">Includere una voce nella [tabella UIText](uitext-table.md) con ScriptInProgress specificato nel campo chiave.</span><span class="sxs-lookup"><span data-stu-id="e0069-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="e0069-121">Specificare il messaggio preliminare come stringa di testo nel campo di testo della tabella UIText.</span><span class="sxs-lookup"><span data-stu-id="e0069-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="e0069-122">Quindi, durante la compilazione dello script, il programma di installazione visualizzerà questa stringa all'interno del controllo di testo.</span><span class="sxs-lookup"><span data-stu-id="e0069-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="e0069-123">Il testo visualizzato scompare non appena la compilazione dello script è terminata.</span><span class="sxs-lookup"><span data-stu-id="e0069-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="e0069-124">Lo stesso controllo di testo che sottoscrive ScriptInProgress ControlEvent può inoltre sottoscrivere [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="e0069-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="e0069-125">In questo caso, poiché il testo della stringa ScriptInProgress preliminare scompare, viene sostituito dalla stringa "tempo rimanente: XX minuti".</span><span class="sxs-lookup"><span data-stu-id="e0069-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



