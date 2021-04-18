---
description: Il programma di installazione utilizza questo evento per pubblicare i dati nell'ultima azione. I dati possono essere visualizzati in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ControlEvent ActionData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311090"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="abf71-105">ControlEvent ActionData</span><span class="sxs-lookup"><span data-stu-id="abf71-105">ActionData ControlEvent</span></span>

<span data-ttu-id="abf71-106">Il programma di installazione utilizza questo evento per pubblicare i dati nell'ultima azione.</span><span class="sxs-lookup"><span data-stu-id="abf71-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="abf71-107">I dati possono essere visualizzati in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent.</span><span class="sxs-lookup"><span data-stu-id="abf71-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="abf71-108">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="abf71-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="abf71-109">Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="abf71-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="abf71-110">Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="abf71-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="abf71-111">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="abf71-111">Published By</span></span>

<span data-ttu-id="abf71-112">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="abf71-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="abf71-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="abf71-113">Argument</span></span>

<span data-ttu-id="abf71-114">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="abf71-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="abf71-115">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="abf71-115">Action on Subscribers</span></span>

<span data-ttu-id="abf71-116">I sottoscrittori sono nascosti quando viene avviata una nuova azione che viene visualizzata quando i nuovi dati di azione arrivano dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="abf71-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="abf71-117">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="abf71-117">Typical Use</span></span>

<span data-ttu-id="abf71-118">Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="abf71-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="abf71-119">L' [attributo di controllo Text](text-control-attribute.md) è elencato nel campo Attributes della tabella per ricevere i dati dell'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="abf71-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="abf71-120">Usato in genere per visualizzare i nomi dei file copiati durante la copia del file.</span><span class="sxs-lookup"><span data-stu-id="abf71-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



