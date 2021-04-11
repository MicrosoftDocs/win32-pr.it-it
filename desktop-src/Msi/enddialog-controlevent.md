---
description: Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale. In tutti i casi il programma di installazione rimuove la finestra di dialogo corrente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: ControlEvent EndDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231878"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="10a1b-104">ControlEvent EndDialog</span><span class="sxs-lookup"><span data-stu-id="10a1b-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="10a1b-105">Questo evento notifica al programma di installazione di rimuovere una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="10a1b-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="10a1b-106">In tutti i casi il programma di installazione rimuove la finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="10a1b-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="10a1b-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="10a1b-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="10a1b-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="10a1b-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="10a1b-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="10a1b-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="10a1b-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="10a1b-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="10a1b-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="10a1b-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="10a1b-112">La tabella seguente elenca l'azione dell'evento risultante da argomenti diversi immessi nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="10a1b-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="10a1b-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="10a1b-113">Argument</span></span> | <span data-ttu-id="10a1b-114">Azione eseguita dal programma di installazione</span><span class="sxs-lookup"><span data-stu-id="10a1b-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10a1b-115">Esci</span><span class="sxs-lookup"><span data-stu-id="10a1b-115">Exit</span></span>     | <span data-ttu-id="10a1b-116">La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore UserExit.</span><span class="sxs-lookup"><span data-stu-id="10a1b-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="10a1b-117">Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="10a1b-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="10a1b-118">Riprova</span><span class="sxs-lookup"><span data-stu-id="10a1b-118">Retry</span></span>    | <span data-ttu-id="10a1b-119">La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore Suspend.</span><span class="sxs-lookup"><span data-stu-id="10a1b-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="10a1b-120">Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="10a1b-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="10a1b-121">Ignora</span><span class="sxs-lookup"><span data-stu-id="10a1b-121">Ignore</span></span>   | <span data-ttu-id="10a1b-122">La sequenza della procedura guidata viene chiusa e il controllo torna al programma di installazione con il valore terminato.</span><span class="sxs-lookup"><span data-stu-id="10a1b-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="10a1b-123">Questo argomento non può essere utilizzato in una finestra di dialogo figlio di un'altra finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="10a1b-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="10a1b-124">Return</span><span class="sxs-lookup"><span data-stu-id="10a1b-124">Return</span></span>   | <span data-ttu-id="10a1b-125">Il controllo torna all'elemento padre della finestra di dialogo presente o, se non è presente alcun elemento padre, il controllo torna al programma di installazione con il valore di operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="10a1b-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="10a1b-126">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="10a1b-126">Published By</span></span>

<span data-ttu-id="10a1b-127">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="10a1b-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="10a1b-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="10a1b-128">Argument</span></span>

<span data-ttu-id="10a1b-129">Nelle finestre di dialogo normali la colonna Argument della [tabella ControlEvent](controlevent-table.md) può essere "Return", "Exit", "Retry" o "ignore".</span><span class="sxs-lookup"><span data-stu-id="10a1b-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="10a1b-130">Nelle finestre di dialogo di errore la colonna Argument della [tabella ControlEvent](controlevent-table.md) può essere "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" o "errorno".</span><span class="sxs-lookup"><span data-stu-id="10a1b-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="10a1b-131">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="10a1b-131">Action on Subscribers</span></span>

<span data-ttu-id="10a1b-132">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="10a1b-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="10a1b-133">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="10a1b-133">Typical Use</span></span>

<span data-ttu-id="10a1b-134">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per chiudere una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="10a1b-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



