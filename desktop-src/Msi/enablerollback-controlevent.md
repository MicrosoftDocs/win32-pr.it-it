---
description: Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: ControlEvent EnableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309486"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="85d8b-103">ControlEvent EnableRollback</span><span class="sxs-lookup"><span data-stu-id="85d8b-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="85d8b-104">Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="85d8b-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="85d8b-105">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="85d8b-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="85d8b-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="85d8b-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="85d8b-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="85d8b-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="85d8b-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="85d8b-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="85d8b-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="85d8b-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="85d8b-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="85d8b-110">Published By</span></span>

<span data-ttu-id="85d8b-111">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="85d8b-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="85d8b-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="85d8b-112">Argument</span></span>

<span data-ttu-id="85d8b-113">False disattiva le funzionalità di rollback del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="85d8b-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="85d8b-114">True attiva le funzionalità di rollback del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="85d8b-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="85d8b-115">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="85d8b-115">Action on Subscribers</span></span>

<span data-ttu-id="85d8b-116">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="85d8b-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="85d8b-117">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="85d8b-117">Typical Use</span></span>

<span data-ttu-id="85d8b-118">Può essere usato per disattivare le funzionalità di rollback se il programma di installazione rileva che lo spazio disponibile su disco è insufficiente per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="85d8b-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="85d8b-119">In questo caso, ControlEvent deve essere usato con le proprietà [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .</span><span class="sxs-lookup"><span data-stu-id="85d8b-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



