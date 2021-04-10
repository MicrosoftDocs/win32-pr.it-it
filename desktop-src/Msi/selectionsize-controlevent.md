---
description: Il controllo SelectionTree usa l'evento SelectionSize per pubblicare la dimensione dell'elemento evidenziato.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: ControlEvent SelectionSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231857"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="0a029-103">ControlEvent SelectionSize</span><span class="sxs-lookup"><span data-stu-id="0a029-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="0a029-104">Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionSize per pubblicare la dimensione dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="0a029-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="0a029-105">Se è un elemento padre, viene pubblicato anche il numero di elementi figlio selezionati.</span><span class="sxs-lookup"><span data-stu-id="0a029-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="0a029-106">La stringa è una delle stringhe **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** o **SelParentCostNegNeg** della [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a029-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="0a029-107">Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a029-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="0a029-108">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0a029-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="0a029-109">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0a029-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="0a029-110">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0a029-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="0a029-111">Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="0a029-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="0a029-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="0a029-112">Published By</span></span>

[<span data-ttu-id="0a029-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="0a029-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="0a029-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="0a029-114">Argument</span></span>

<span data-ttu-id="0a029-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="0a029-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0a029-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="0a029-116">Action on Subscribers</span></span>

<span data-ttu-id="0a029-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="0a029-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0a029-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="0a029-118">Typical Use</span></span>

<span data-ttu-id="0a029-119">Controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del controllo SelectionTree tramite la [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a029-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="0a029-120">Il controllo testo usa questo evento per visualizzare la dimensione dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="0a029-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



