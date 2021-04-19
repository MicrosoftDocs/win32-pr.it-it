---
description: Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia scrivibile. Se non è possibile scrivere il percorso, l'evento blocca ulteriormente ControlEvents associati al controllo.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: ControlEvent CheckExistingTargetPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310988"
---
# <a name="checkexistingtargetpath-controlevent"></a><span data-ttu-id="68ed7-104">ControlEvent CheckExistingTargetPath</span><span class="sxs-lookup"><span data-stu-id="68ed7-104">CheckExistingTargetPath ControlEvent</span></span>

<span data-ttu-id="68ed7-105">Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia scrivibile.</span><span class="sxs-lookup"><span data-stu-id="68ed7-105">This event notifies the installer that it has to verify that the selected path is writable.</span></span> <span data-ttu-id="68ed7-106">Se non è possibile scrivere il percorso, l'evento blocca ulteriormente ControlEvents associati al controllo.</span><span class="sxs-lookup"><span data-stu-id="68ed7-106">If the path is cannot be written, then the event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="68ed7-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="68ed7-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="68ed7-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="68ed7-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="68ed7-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="68ed7-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="68ed7-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="68ed7-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="68ed7-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="68ed7-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="68ed7-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="68ed7-112">Published By</span></span>

<span data-ttu-id="68ed7-113">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="68ed7-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="68ed7-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="68ed7-114">Argument</span></span>

<span data-ttu-id="68ed7-115">Nome della proprietà che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="68ed7-115">The name of the property containing the path.</span></span> <span data-ttu-id="68ed7-116">Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="68ed7-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="68ed7-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="68ed7-117">Action on Subscribers</span></span>

<span data-ttu-id="68ed7-118">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="68ed7-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="68ed7-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="68ed7-119">Typical Use</span></span>

<span data-ttu-id="68ed7-120">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo di esplorazione è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="68ed7-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

 

 



