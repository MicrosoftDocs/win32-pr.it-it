---
description: Questo evento notifica al controllo Directory che l'utente desidera selezionare l'elemento padre della directory corrente. Per informazioni correlate, vedere finestra di dialogo Sfoglia.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: ControlEvent DirectoryListUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968757"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="4007c-104">ControlEvent DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="4007c-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="4007c-105">Questo evento notifica al [controllo Directory](directorylist-control.md) che l'utente desidera selezionare l'elemento padre della directory corrente.</span><span class="sxs-lookup"><span data-stu-id="4007c-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="4007c-106">Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="4007c-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="4007c-107">Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento.</span><span class="sxs-lookup"><span data-stu-id="4007c-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="4007c-108">L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="4007c-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="4007c-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="4007c-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="4007c-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4007c-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="4007c-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="4007c-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="4007c-112">Se la directory corrente è la directory radice dell'unità, un evento DirectoryListUp Disabilita tutti gli altri controlli che pubblicano un evento DirectoryListUp.</span><span class="sxs-lookup"><span data-stu-id="4007c-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="4007c-113">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="4007c-113">Published By</span></span>

[<span data-ttu-id="4007c-114">Elenco di directory</span><span class="sxs-lookup"><span data-stu-id="4007c-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="4007c-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="4007c-115">Argument</span></span>

<span data-ttu-id="4007c-116">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="4007c-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="4007c-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="4007c-117">Action on Subscribers</span></span>

<span data-ttu-id="4007c-118">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="4007c-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="4007c-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="4007c-119">Typical Use</span></span>

<span data-ttu-id="4007c-120">Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale in cui si trova l'elenco di directory viene utilizzato per attivare l'esecuzione nel percorso.</span><span class="sxs-lookup"><span data-stu-id="4007c-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



