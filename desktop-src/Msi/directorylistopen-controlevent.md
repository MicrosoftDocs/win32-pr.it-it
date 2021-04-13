---
description: Questo evento seleziona ed evidenzia una directory nel controllo Directory che l'utente ha scelto di aprire. Per informazioni correlate, vedere finestra di dialogo Sfoglia.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: ControlEvent DirectoryListOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234354"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="b8062-104">ControlEvent DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="b8062-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="b8062-105">Questo evento seleziona ed evidenzia una directory nel [controllo Directory](directorylist-control.md) che l'utente ha scelto di aprire.</span><span class="sxs-lookup"><span data-stu-id="b8062-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="b8062-106">Per informazioni correlate, vedere [finestra di dialogo Sfoglia](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="b8062-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="b8062-107">Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento.</span><span class="sxs-lookup"><span data-stu-id="b8062-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="b8062-108">L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b8062-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="b8062-109">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b8062-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b8062-110">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b8062-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="b8062-111">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b8062-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="b8062-112">Se non è stata selezionata alcuna directory nel [controllo Directory](directorylist-control.md), un evento DirectoryListOpen Disabilita tutti gli altri controlli che pubblicano un evento DirectoryListOpen.</span><span class="sxs-lookup"><span data-stu-id="b8062-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="b8062-113">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="b8062-113">Published By</span></span>

[<span data-ttu-id="b8062-114">Elenco di directory</span><span class="sxs-lookup"><span data-stu-id="b8062-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="b8062-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="b8062-115">Argument</span></span>

<span data-ttu-id="b8062-116">Questo ControlEvent non usa un argomento.</span><span class="sxs-lookup"><span data-stu-id="b8062-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="b8062-117">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="b8062-117">Action on Subscribers</span></span>

<span data-ttu-id="b8062-118">Questo ControlEvent non esegue alcuna azione nei Sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="b8062-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="b8062-119">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="b8062-119">Typical Use</span></span>

<span data-ttu-id="b8062-120">Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale in cui si trova l'elenco di directory viene usato per attivare l'istruzione/routine nel percorso.</span><span class="sxs-lookup"><span data-stu-id="b8062-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



