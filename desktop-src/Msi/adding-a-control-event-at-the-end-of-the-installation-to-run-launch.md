---
description: Il programma di installazione esegue la sequenza di installazione guidata dell'esempio solo se viene usato il livello di interfaccia utente completo per installare l'applicazione.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967301"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="73dec-103">Aggiunta di un evento di controllo alla fine dell'installazione per l'esecuzione dell'avvio</span><span class="sxs-lookup"><span data-stu-id="73dec-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="73dec-104">Il programma di installazione esegue la sequenza di installazione guidata dell'esempio solo se viene usato il livello di [*interfaccia utente completo*](f-gly.md) per installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73dec-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="73dec-105">L'ultima finestra di dialogo della sequenza di finestra di dialogo di esempio è una finestra di dialogo di [uscita](exit-dialog.md) denominata ExitDialog.</span><span class="sxs-lookup"><span data-stu-id="73dec-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="73dec-106">Quando un utente interagisce con il pulsante OK in ExitDialog, questa prima pubblica un [EndDialog ControlEvent](enddialog-controlevent.md) che restituisce il controllo al programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="73dec-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="73dec-107">Il controllo pubblica quindi un [ControlEvent DoAction](doaction-controlevent.md) che esegue l'azione personalizzata Launch.</span><span class="sxs-lookup"><span data-stu-id="73dec-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="73dec-108">Ogni evento di controllo richiede un record nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="73dec-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="73dec-109">Vedere [Panoramica di ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73dec-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="73dec-110">Tabella ControlEvent</span><span class="sxs-lookup"><span data-stu-id="73dec-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="73dec-111">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="73dec-111">Dialog</span></span>     | <span data-ttu-id="73dec-112">controllo\_</span><span class="sxs-lookup"><span data-stu-id="73dec-112">Control\_</span></span> | <span data-ttu-id="73dec-113">Evento</span><span class="sxs-lookup"><span data-stu-id="73dec-113">Event</span></span>     | <span data-ttu-id="73dec-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="73dec-114">Argument</span></span> | <span data-ttu-id="73dec-115">Condizione</span><span class="sxs-lookup"><span data-stu-id="73dec-115">Condition</span></span>                     | <span data-ttu-id="73dec-116">Ordering</span><span class="sxs-lookup"><span data-stu-id="73dec-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="73dec-117">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="73dec-117">ExitDialog</span></span> | <span data-ttu-id="73dec-118">OK</span><span class="sxs-lookup"><span data-stu-id="73dec-118">OK</span></span>        | <span data-ttu-id="73dec-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="73dec-119">EndDialog</span></span> | <span data-ttu-id="73dec-120">Return</span><span class="sxs-lookup"><span data-stu-id="73dec-120">Return</span></span>   | <span data-ttu-id="73dec-121">1</span><span class="sxs-lookup"><span data-stu-id="73dec-121">1</span></span>                             | <span data-ttu-id="73dec-122">1</span><span class="sxs-lookup"><span data-stu-id="73dec-122">1</span></span>        |
| <span data-ttu-id="73dec-123">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="73dec-123">ExitDialog</span></span> | <span data-ttu-id="73dec-124">OK</span><span class="sxs-lookup"><span data-stu-id="73dec-124">OK</span></span>        | <span data-ttu-id="73dec-125">DoAction</span><span class="sxs-lookup"><span data-stu-id="73dec-125">DoAction</span></span>  | <span data-ttu-id="73dec-126">Launch</span><span class="sxs-lookup"><span data-stu-id="73dec-126">Launch</span></span>   | <span data-ttu-id="73dec-127">NON installato e $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="73dec-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="73dec-128">2</span><span class="sxs-lookup"><span data-stu-id="73dec-128">2</span></span>        |



 

<span data-ttu-id="73dec-129">La condizione sul controllo DoAction garantisce che l'azione personalizzata venga eseguita solo durante la prima installazione dell'applicazione e che venga installata localmente.</span><span class="sxs-lookup"><span data-stu-id="73dec-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="73dec-130">La frase $Tutorial = 3 indica che lo stato dell'azione del componente tutorial è impostato su local.</span><span class="sxs-lookup"><span data-stu-id="73dec-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="73dec-131">Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="73dec-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="73dec-132">Questa operazione completa l'esempio.</span><span class="sxs-lookup"><span data-stu-id="73dec-132">This completes the sample.</span></span>

 

 



