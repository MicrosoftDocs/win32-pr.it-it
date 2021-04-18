---
description: Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia valido. Se il percorso non è valido, questo evento blocca ulteriormente ControlEvents associati al controllo.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: ControlEvent CheckTargetPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310983"
---
# <a name="checktargetpath-controlevent"></a><span data-ttu-id="ab649-104">ControlEvent CheckTargetPath</span><span class="sxs-lookup"><span data-stu-id="ab649-104">CheckTargetPath ControlEvent</span></span>

<span data-ttu-id="ab649-105">Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia valido.</span><span class="sxs-lookup"><span data-stu-id="ab649-105">This event notifies the installer that it has to verify that the selected path is valid.</span></span> <span data-ttu-id="ab649-106">Se il percorso non è valido, questo evento blocca ulteriormente ControlEvents associati al controllo.</span><span class="sxs-lookup"><span data-stu-id="ab649-106">If the path is not valid, then this event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="ab649-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="ab649-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="ab649-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="ab649-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="ab649-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ab649-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ab649-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ab649-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ab649-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ab649-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ab649-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="ab649-112">Published By</span></span>

<span data-ttu-id="ab649-113">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ab649-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ab649-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="ab649-114">Argument</span></span>

<span data-ttu-id="ab649-115">Nome della proprietà che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="ab649-115">The name of the property containing the path.</span></span> <span data-ttu-id="ab649-116">Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="ab649-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ab649-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="ab649-117">Action on Subscribers</span></span>

<span data-ttu-id="ab649-118">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="ab649-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ab649-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="ab649-119">Typical Use</span></span>

<span data-ttu-id="ab649-120">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo Sfoglia è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="ab649-120">A [PushButton](pushbutton-control.md) control on a browse dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog box.</span></span>

 

 



