---
description: Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo. Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: ControlEvent NewDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130674"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="b8254-104">ControlEvent NewDialog</span><span class="sxs-lookup"><span data-stu-id="b8254-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="b8254-105">Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b8254-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="b8254-106">Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento.</span><span class="sxs-lookup"><span data-stu-id="b8254-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="b8254-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="b8254-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="b8254-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8254-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="b8254-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8254-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b8254-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8254-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b8254-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b8254-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b8254-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="b8254-112">Published By</span></span>

<span data-ttu-id="b8254-113">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b8254-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b8254-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="b8254-114">Argument</span></span>

<span data-ttu-id="b8254-115">Stringa che rappresenta il nome della nuova finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b8254-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b8254-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="b8254-116">Action on Subscribers</span></span>

<span data-ttu-id="b8254-117">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="b8254-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b8254-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="b8254-118">Typical Use</span></span>

<span data-ttu-id="b8254-119">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per segnalare una transizione alla finestra di dialogo successiva o precedente della stessa sequenza della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="b8254-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



