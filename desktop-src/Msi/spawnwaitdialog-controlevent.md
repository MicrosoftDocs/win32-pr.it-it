---
description: Il ControlEvent SpawnWaitDialog attiva la finestra di dialogo specificata dalla colonna Argument della tabella ControlEvent, se l'espressione nella colonna condizione restituisce FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: ControlEvent SpawnWaitDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966786"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="5ede8-103">ControlEvent SpawnWaitDialog</span><span class="sxs-lookup"><span data-stu-id="5ede8-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="5ede8-104">Il ControlEvent SpawnWaitDialog attiva la finestra di dialogo specificata dalla colonna Argument della [tabella ControlEvent](controlevent-table.md), se l'espressione nella colonna condizione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="5ede8-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="5ede8-105">La finestra di dialogo rimane attiva fino a quando l'espressione condizionale rimane FALSE e viene rimossa non appena la condizione restituisce TRUE.</span><span class="sxs-lookup"><span data-stu-id="5ede8-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="5ede8-106">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="5ede8-107">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="5ede8-108">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5ede8-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5ede8-109">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5ede8-110">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="5ede8-111">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="5ede8-111">Published By</span></span>

<span data-ttu-id="5ede8-112">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="5ede8-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="5ede8-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="5ede8-113">Argument</span></span>

<span data-ttu-id="5ede8-114">Finestra di dialogo nella [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5ede8-115">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="5ede8-115">Action on Subscribers</span></span>

<span data-ttu-id="5ede8-116">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="5ede8-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5ede8-117">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="5ede8-117">Typical Use</span></span>

<span data-ttu-id="5ede8-118">Il ControlEvent SpawnWaitDialog può essere usato per attendere il completamento di un'attività in background, che può essere testata usando un'espressione condizionale, ad esempio lo stato di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ede8-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="5ede8-119">Per un esempio relativo all'uso di SpawnWaitDialog ControlEvent, vedere la sezione [creazione di un condizionale "attendere..." MessageBox](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="5ede8-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



