---
description: Il programma di installazione usa l'evento seprogress per pubblicare informazioni sullo stato di avanzamento dell'installazione.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: ControlEvent di avanzamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967904"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="a59b5-103">ControlEvent di avanzamento</span><span class="sxs-lookup"><span data-stu-id="a59b5-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="a59b5-104">Il programma di installazione usa l'evento seprogress per pubblicare informazioni sullo stato di avanzamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="a59b5-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="a59b5-105">Un controllo [ProgressBar](progressbar-control.md) o un [controllo Billboard](billboard-control.md) deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md) assegnando un nome all'azione di cui viene indicato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a59b5-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="a59b5-106">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a59b5-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a59b5-107">Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a59b5-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="a59b5-108">Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a59b5-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a59b5-109">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="a59b5-109">Published By</span></span>

<span data-ttu-id="a59b5-110">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="a59b5-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a59b5-111">Argomento</span><span class="sxs-lookup"><span data-stu-id="a59b5-111">Argument</span></span>

<span data-ttu-id="a59b5-112">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a59b5-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a59b5-113">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="a59b5-113">Action on Subscribers</span></span>

<span data-ttu-id="a59b5-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a59b5-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a59b5-115">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="a59b5-115">Typical Use</span></span>

<span data-ttu-id="a59b5-116">Un controllo [ProgressBar](progressbar-control.md) in una finestra di dialogo non modale sottoscrive questo evento usando l'attributo [Progress](progress-control-attribute.md) per ricevere le informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="a59b5-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



