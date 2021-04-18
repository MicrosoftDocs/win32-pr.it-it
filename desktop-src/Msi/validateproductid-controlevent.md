---
description: L'evento ValidateProductID imposta la proprietà ProductID sull'ID prodotto completo. Se la convalida ha esito negativo, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ControlEvent ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308172"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="c8096-104">ControlEvent ValidateProductID</span><span class="sxs-lookup"><span data-stu-id="c8096-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="c8096-105">L'evento ValidateProductID imposta la proprietà [**ProductID**](productid.md) sull'ID prodotto completo.</span><span class="sxs-lookup"><span data-stu-id="c8096-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="c8096-106">Se la convalida ha esito negativo, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="c8096-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="c8096-107">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="c8096-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="c8096-108">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8096-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="c8096-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c8096-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c8096-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c8096-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c8096-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c8096-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c8096-112">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="c8096-112">Published By</span></span>

<span data-ttu-id="c8096-113">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c8096-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c8096-114">Argomento</span><span class="sxs-lookup"><span data-stu-id="c8096-114">Argument</span></span>

<span data-ttu-id="c8096-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="c8096-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c8096-116">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="c8096-116">Action on Subscribers</span></span>

<span data-ttu-id="c8096-117">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="c8096-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c8096-118">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="c8096-118">Typical Use</span></span>

<span data-ttu-id="c8096-119">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e viene usato per controllare la voce dell'utente dell'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="c8096-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="c8096-120">Se la voce dell'utente è valida, verrà visualizzata la finestra di dialogo successiva.</span><span class="sxs-lookup"><span data-stu-id="c8096-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



