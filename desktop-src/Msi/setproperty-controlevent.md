---
description: "La sintassi per l'evento SetProperty è diversa da quella per altri ControlEvents al posto del nome dell'evento. uno inserisce la proprietà tra parentesi quadre: \\[ nome della \\_ proprietà \\] ."
ms.assetid: a8e80d14-8d62-4398-9e53-9a0119a62d70
title: Proprietà ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59326ddd9f576b4871de7c232318ffcdcdb4fb36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314776"
---
# <a name="setproperty-controlevent"></a><span data-ttu-id="80cc4-103">Proprietà ControlEvent</span><span class="sxs-lookup"><span data-stu-id="80cc4-103">SetProperty ControlEvent</span></span>

<span data-ttu-id="80cc4-104">La sintassi per l'evento SetProperty è diversa da quella per altri ControlEvents al posto del nome dell'evento. uno inserisce la proprietà tra parentesi quadre: \[ nome della \_ proprietà \] .</span><span class="sxs-lookup"><span data-stu-id="80cc4-104">The syntax for the SetProperty event is different than for other ControlEvents In place of the name of the event one puts the property in square brackets: \[property\_name\].</span></span> <span data-ttu-id="80cc4-105">L'argomento è il nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="80cc4-105">The argument is the new value of the property.</span></span> <span data-ttu-id="80cc4-106">Per annullare la proprietà, l'argomento deve essere {} .</span><span class="sxs-lookup"><span data-stu-id="80cc4-106">To unset the property, the argument must be {}.</span></span> <span data-ttu-id="80cc4-107">Questa operazione è necessaria perché l'argomento è una chiave primaria nella tabella e quindi non può essere null.</span><span class="sxs-lookup"><span data-stu-id="80cc4-107">This is necessary, because the argument is a primary key in the table and so cannot be null.</span></span> <span data-ttu-id="80cc4-108">L'argomento verrà formattato con il metodo FormatText, pertanto l'argomento può contenere qualsiasi espressione che il metodo FormatText è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="80cc4-108">The argument will be formatted using the FormatText method, therefore the argument can contain any expression that the FormatText method can handle.</span></span> <span data-ttu-id="80cc4-109">I valori delle proprietà vengono valutati al momento del ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="80cc4-109">The property values are evaluated at the moment of the ControlEvent.</span></span>

<span data-ttu-id="80cc4-110">Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="80cc4-110">This event can be published by a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="80cc4-111">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="80cc4-111">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="80cc4-112">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="80cc4-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="80cc4-113">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="80cc4-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="80cc4-114">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="80cc4-114">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="80cc4-115">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="80cc4-115">Published By</span></span>

<span data-ttu-id="80cc4-116">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="80cc4-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="80cc4-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="80cc4-117">Argument</span></span>

<span data-ttu-id="80cc4-118">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="80cc4-118">The new value of the property.</span></span> <span data-ttu-id="80cc4-119">{} per null.</span><span class="sxs-lookup"><span data-stu-id="80cc4-119">{} for null.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="80cc4-120">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="80cc4-120">Action on Subscribers</span></span>

<span data-ttu-id="80cc4-121">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="80cc4-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="80cc4-122">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="80cc4-122">Typical Use</span></span>

<span data-ttu-id="80cc4-123">Controllo [pulsante](pushbutton-control.md) in una finestra di dialogo collegata a questo evento in modo che modifichi una proprietà quando viene eseguito il push del pulsante.</span><span class="sxs-lookup"><span data-stu-id="80cc4-123">A [PushButton](pushbutton-control.md) control on a dialog box linked to this event so it changes a property when the button is pushed.</span></span>

 

 



