---
description: Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo di permanenza approssimativo, in secondi, per la sequenza di avanzamento corrente.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: ControlEvent TimeRemaining
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058184"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="a54b6-103">ControlEvent TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="a54b6-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="a54b6-104">Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo di permanenza approssimativo, in secondi, per la sequenza di avanzamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a54b6-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="a54b6-105">Il tempo rimanente può essere visualizzato in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="a54b6-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="a54b6-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a54b6-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a54b6-107">Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a54b6-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="a54b6-108">Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a54b6-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a54b6-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="a54b6-109">Published By</span></span>

<span data-ttu-id="a54b6-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="a54b6-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a54b6-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="a54b6-111">Argument</span></span>

<span data-ttu-id="a54b6-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a54b6-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a54b6-113">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="a54b6-113">Action on Subscribers</span></span>

<span data-ttu-id="a54b6-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a54b6-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a54b6-115">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="a54b6-115">Typical Use</span></span>

<span data-ttu-id="a54b6-116">Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md) e utilizza l' [attributo TimeRemaining](timeremaining-control-attribute.md) per visualizzare il tempo rimanente.</span><span class="sxs-lookup"><span data-stu-id="a54b6-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="a54b6-117">Lo stesso controllo di testo che sottoscrive TimeRemaining ControlEvent può inoltre sottoscrivere [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a54b6-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="a54b6-118">In questo caso, come la stringa di messaggio ScriptInProgress preliminare, viene sostituita dalla stringa "tempo rimanente: XX minuti".</span><span class="sxs-lookup"><span data-stu-id="a54b6-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



