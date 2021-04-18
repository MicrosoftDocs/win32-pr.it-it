---
description: Il controllo SelectionTree usa l'evento SelectionDescription per pubblicare una stringa che contiene la descrizione dell'elemento evidenziato. Questa stringa è il campo della descrizione della tabella delle funzionalità. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: ControlEvent SelectionDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313332"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="6d19d-105">ControlEvent SelectionDescription</span><span class="sxs-lookup"><span data-stu-id="6d19d-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="6d19d-106">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionDescription per pubblicare una stringa che contiene la descrizione dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="6d19d-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="6d19d-107">Questa stringa è il campo della **Descrizione** della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="6d19d-108">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="6d19d-109">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="6d19d-110">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6d19d-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="6d19d-111">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="6d19d-112">Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="6d19d-113">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="6d19d-113">Published By</span></span>

[<span data-ttu-id="6d19d-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="6d19d-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="6d19d-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="6d19d-115">Argument</span></span>

<span data-ttu-id="6d19d-116">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6d19d-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6d19d-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="6d19d-117">Action on Subscribers</span></span>

<span data-ttu-id="6d19d-118">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6d19d-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6d19d-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="6d19d-119">Typical Use</span></span>

<span data-ttu-id="6d19d-120">Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree sottoscrive questo ControlEvent tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d19d-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="6d19d-121">Il controllo testo usa questo evento per visualizzare la descrizione dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="6d19d-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



