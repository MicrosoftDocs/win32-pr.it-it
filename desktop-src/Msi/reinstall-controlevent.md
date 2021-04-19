---
description: Consente all'autore di avviare una reinstallazione di alcune o di tutte le funzionalità, mentre è in esecuzione la finestra di dialogo corrente.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstallare ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311700"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="f9394-103">Reinstallare ControlEvent</span><span class="sxs-lookup"><span data-stu-id="f9394-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="f9394-104">Reinstallare ControlEventallows l'autore per avviare una reinstallazione di alcune o di tutte le funzionalità, mentre è in esecuzione la finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="f9394-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="f9394-105">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md) o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="f9394-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="f9394-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md)e richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f9394-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f9394-107">Questo evento non funziona con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f9394-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f9394-108">Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f9394-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f9394-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="f9394-109">Published By</span></span>

<span data-ttu-id="f9394-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="f9394-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f9394-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="f9394-111">Argument</span></span>

<span data-ttu-id="f9394-112">Stringa che rappresenta il nome della funzionalità o "ALL".</span><span class="sxs-lookup"><span data-stu-id="f9394-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f9394-113">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="f9394-113">Action on Subscribers</span></span>

<span data-ttu-id="f9394-114">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="f9394-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f9394-115">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="f9394-115">Typical Use</span></span>

<span data-ttu-id="f9394-116">Questo evento è associato a un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="f9394-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="f9394-117">Lo stesso controllo [pulsante](pushbutton-control.md) deve essere associato anche a un ControlEvent [REINSTALLMODE](reinstallmode-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="f9394-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



