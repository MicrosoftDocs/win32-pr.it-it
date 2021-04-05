---
description: Il programma di installazione utilizza questo evento per pubblicare il nome dell'azione corrente. Il nome può essere visualizzato in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ControlEvent ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967303"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="b9124-105">ControlEvent ActionText</span><span class="sxs-lookup"><span data-stu-id="b9124-105">ActionText ControlEvent</span></span>

<span data-ttu-id="b9124-106">Il programma di installazione utilizza questo evento per pubblicare il nome dell'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="b9124-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="b9124-107">Il nome può essere visualizzato in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="b9124-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="b9124-108">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9124-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b9124-109">Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b9124-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="b9124-110">Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b9124-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="b9124-111">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="b9124-111">Published By</span></span>

<span data-ttu-id="b9124-112">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9124-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="b9124-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="b9124-113">Argument</span></span>

<span data-ttu-id="b9124-114">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="b9124-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b9124-115">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="b9124-115">Action on Subscribers</span></span>

<span data-ttu-id="b9124-116">I sottoscrittori vengono visualizzati quando i nuovi dati di stato arrivano dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9124-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b9124-117">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="b9124-117">Typical Use</span></span>

<span data-ttu-id="b9124-118">Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b9124-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="b9124-119">L' [attributo del controllo testo](text-control-attribute.md) deve essere elencato nel campo attributi di questa tabella per ricevere il nome dell'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="b9124-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



