---
description: Il programma di installazione riceve una notifica tramite questo evento quando una funzionalità o tutte le funzionalità sono selezionate per la rimozione mantenendo la finestra di dialogo corrente.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Rimuovere ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312323"
---
# <a name="remove-controlevent"></a><span data-ttu-id="5110c-103">Rimuovere ControlEvent</span><span class="sxs-lookup"><span data-stu-id="5110c-103">Remove ControlEvent</span></span>

<span data-ttu-id="5110c-104">Il programma di installazione riceve una notifica tramite questo evento quando una funzionalità o tutte le funzionalità sono selezionate per la rimozione mantenendo la finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="5110c-104">The installer is notified through this event when a feature or all features are selected for removal while keeping the present dialog box running.</span></span>

<span data-ttu-id="5110c-105">Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="5110c-105">This event can be published by a [PushButton control](pushbutton-control.md), [CheckBox control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="5110c-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="5110c-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="5110c-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="5110c-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="5110c-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5110c-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="5110c-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5110c-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="5110c-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="5110c-110">Published By</span></span>

<span data-ttu-id="5110c-111">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="5110c-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="5110c-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="5110c-112">Argument</span></span>

<span data-ttu-id="5110c-113">Stringa che rappresenta il nome della funzionalità o "ALL".</span><span class="sxs-lookup"><span data-stu-id="5110c-113">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="5110c-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="5110c-114">Action on Subscribers</span></span>

<span data-ttu-id="5110c-115">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="5110c-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="action-by-publisher-when-subscriber-activated"></a><span data-ttu-id="5110c-116">Azione per autore quando il Sottoscrittore è attivato</span><span class="sxs-lookup"><span data-stu-id="5110c-116">Action by Publisher When Subscriber Activated</span></span>

<span data-ttu-id="5110c-117">Il programma di installazione mantiene la finestra di dialogo in esecuzione e invia una notifica al programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="5110c-117">The installer keeps the present dialog box running and notifies the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="5110c-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="5110c-118">Typical Use</span></span>

<span data-ttu-id="5110c-119">Controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale associata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="5110c-119">A [PushButton](pushbutton-control.md) control on a modal dialog box tied to this event.</span></span>

 

 



