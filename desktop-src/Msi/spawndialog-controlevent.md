---
description: Il ControlEvent SpawnDialog notifica al programma di installazione di creare un elemento figlio di una finestra di dialogo modale mantenendo la finestra di dialogo in esecuzione.
ms.assetid: 2a341039-60dd-4e6c-9ef3-bf482ca53917
title: ControlEvent SpawnDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71aec632332a87d047913b618aa2c39843849e5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305960"
---
# <a name="spawndialog-controlevent"></a><span data-ttu-id="c9c55-103">ControlEvent SpawnDialog</span><span class="sxs-lookup"><span data-stu-id="c9c55-103">SpawnDialog ControlEvent</span></span>

<span data-ttu-id="c9c55-104">Il ControlEvent SpawnDialog notifica al programma di installazione di creare un elemento figlio di una finestra di dialogo modale mantenendo la finestra di dialogo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c9c55-104">The SpawnDialog ControlEvent notifies the installer to create a child of a modal dialog box while keeping the present dialog box running.</span></span>

<span data-ttu-id="c9c55-105">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="c9c55-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="c9c55-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9c55-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="c9c55-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c55-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c9c55-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c9c55-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c9c55-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c9c55-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c9c55-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="c9c55-110">Published By</span></span>

<span data-ttu-id="c9c55-111">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c9c55-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="c9c55-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="c9c55-112">Argument</span></span>

<span data-ttu-id="c9c55-113">Stringa che rappresenta il nome della nuova finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c9c55-113">A string that is the name of the new dialog box.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c9c55-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="c9c55-114">Action on Subscribers</span></span>

<span data-ttu-id="c9c55-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="c9c55-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c9c55-116">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="c9c55-116">Typical Use</span></span>

<span data-ttu-id="c9c55-117">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per creare una finestra di dialogo figlio, ad esempio "annullare?"</span><span class="sxs-lookup"><span data-stu-id="c9c55-117">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to create a child dialog, such as an "Are you sure you want to cancel?"</span></span> <span data-ttu-id="c9c55-118">dell'applicazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="c9c55-118">dialog box.</span></span>

 

 



