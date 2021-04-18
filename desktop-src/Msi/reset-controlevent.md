---
description: La finestra di dialogo viene reimpostata. In altre parole, tutti i controlli della finestra di dialogo vengono chiamati per annullare le modifiche apportate alle proprietà. Questo evento Reimposta tutti i valori della proprietà quando è stata creata la finestra di dialogo.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Reimposta ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313794"
---
# <a name="reset-controlevent"></a><span data-ttu-id="b9f36-105">Reimposta ControlEvent</span><span class="sxs-lookup"><span data-stu-id="b9f36-105">Reset ControlEvent</span></span>

<span data-ttu-id="b9f36-106">La finestra di dialogo viene reimpostata.</span><span class="sxs-lookup"><span data-stu-id="b9f36-106">The dialog box is reset.</span></span> <span data-ttu-id="b9f36-107">In altre parole, tutti i controlli della finestra di dialogo vengono chiamati per annullare le modifiche apportate alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="b9f36-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="b9f36-108">Questo evento Reimposta tutti i valori della proprietà quando è stata creata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b9f36-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="b9f36-109">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="b9f36-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="b9f36-110">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9f36-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="b9f36-111">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b9f36-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b9f36-112">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b9f36-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b9f36-113">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b9f36-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="b9f36-114">Un caso, che dovrebbe verificarsi raramente in pratica, non viene gestito correttamente da questo ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="b9f36-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="b9f36-115">Se sono presenti due o più controlli nella stessa finestra di dialogo collegati indirettamente alla stessa proprietà e almeno uno di essi ha iniziato a disporre di un'altra proprietà, il valore di questa proprietà verrà a volte reimpostato sul secondo valore.</span><span class="sxs-lookup"><span data-stu-id="b9f36-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="b9f36-116">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="b9f36-116">Published By</span></span>

<span data-ttu-id="b9f36-117">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9f36-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b9f36-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="b9f36-118">Argument</span></span>

<span data-ttu-id="b9f36-119">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b9f36-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b9f36-120">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="b9f36-120">Action on Subscribers</span></span>

<span data-ttu-id="b9f36-121">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b9f36-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b9f36-122">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="b9f36-122">Typical Use</span></span>

<span data-ttu-id="b9f36-123">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale viene utilizzato per reimpostare tutti i valori nella finestra di dialogo e per annullare tutte le modifiche nella pagina.</span><span class="sxs-lookup"><span data-stu-id="b9f36-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



