---
description: L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato. Se il percorso non è valido per la scrittura in, il programma di installazione blocca ulteriori ControlEvents associate al controllo.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: ControlEvent SetTargetPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232437"
---
# <a name="settargetpath-controlevent"></a><span data-ttu-id="941dd-104">ControlEvent SetTargetPath</span><span class="sxs-lookup"><span data-stu-id="941dd-104">SetTargetPath ControlEvent</span></span>

<span data-ttu-id="941dd-105">L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato.</span><span class="sxs-lookup"><span data-stu-id="941dd-105">The SetTargetPath event notifies the installer to check and set the selected path.</span></span> <span data-ttu-id="941dd-106">Se il percorso non è valido per la scrittura in, il programma di installazione blocca ulteriori ControlEvents associate al controllo.</span><span class="sxs-lookup"><span data-stu-id="941dd-106">If the path is not valid to be written to, then the installer blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="941dd-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="941dd-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="941dd-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="941dd-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="941dd-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="941dd-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="941dd-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="941dd-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="941dd-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="941dd-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="941dd-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="941dd-112">Published By</span></span>

<span data-ttu-id="941dd-113">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="941dd-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="941dd-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="941dd-114">Argument</span></span>

<span data-ttu-id="941dd-115">Nome della proprietà che contiene il percorso.</span><span class="sxs-lookup"><span data-stu-id="941dd-115">The name of the property containing the path.</span></span> <span data-ttu-id="941dd-116">Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="941dd-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="941dd-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="941dd-117">Action on Subscribers</span></span>

<span data-ttu-id="941dd-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="941dd-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="941dd-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="941dd-119">Typical Use</span></span>

<span data-ttu-id="941dd-120">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo di esplorazione è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="941dd-120">A [PushButton](pushbutton-control.md) control on a browse dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog.</span></span>

## <a name="remarks"></a><span data-ttu-id="941dd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="941dd-121">Remarks</span></span>

<span data-ttu-id="941dd-122">Non tentare di configurare il percorso di destinazione se i componenti che utilizzano tali percorsi sono già installati per l'utente corrente o per un altro utente.</span><span class="sxs-lookup"><span data-stu-id="941dd-122">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="941dd-123">Controllare la proprietà [**ProductState**](productstate.md) prima di pubblicare il ControlEvent SetTargetPath per determinare se il prodotto contenente il componente è installato.</span><span class="sxs-lookup"><span data-stu-id="941dd-123">Check the [**ProductState**](productstate.md) property before publishing the SetTargetPath ControlEvent to determine if the product containing the component is installed.</span></span>

 

 



