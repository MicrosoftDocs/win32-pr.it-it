---
description: Consente all'autore di specificare la modalità o le modalità di convalida durante una reinstallazione e mentre è in esecuzione la finestra di dialogo corrente.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ControlEvent ReinstallMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311697"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="d704c-103">ControlEvent ReinstallMode</span><span class="sxs-lookup"><span data-stu-id="d704c-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="d704c-104">ReinstallMode ControlEventallows l'autore per specificare la modalità o le modalità di convalida durante una reinstallazione e durante l'esecuzione della finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="d704c-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="d704c-105">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md) o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d704c-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="d704c-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md)e richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d704c-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d704c-107">Questo evento non funziona con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d704c-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d704c-108">Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d704c-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="d704c-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="d704c-109">Published By</span></span>

<span data-ttu-id="d704c-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="d704c-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d704c-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="d704c-111">Argument</span></span>

<span data-ttu-id="d704c-112">Stringa.</span><span class="sxs-lookup"><span data-stu-id="d704c-112">A string.</span></span> <span data-ttu-id="d704c-113">Per un elenco di valori possibili, vedere proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="d704c-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d704c-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="d704c-114">Action on Subscribers</span></span>

<span data-ttu-id="d704c-115">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="d704c-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d704c-116">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="d704c-116">Typical Use</span></span>

<span data-ttu-id="d704c-117">Questo evento è associato a un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="d704c-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="d704c-118">Lo stesso controllo [pulsante](pushbutton-control.md) deve essere associato anche a un ControlEvent di [Reinstallazione](reinstall-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="d704c-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



