---
description: L'evento SetInstallLevel consente di modificare il livello di installazione impostando il valore specificato dall'argomento.
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: ControlEvent SetInstallLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347f54cee1494b2ff91f7dc1701f0b7749d47e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226353"
---
# <a name="setinstalllevel-controlevent"></a><span data-ttu-id="21190-103">ControlEvent SetInstallLevel</span><span class="sxs-lookup"><span data-stu-id="21190-103">SetInstallLevel ControlEvent</span></span>

<span data-ttu-id="21190-104">L'evento SetInstallLevel consente di modificare il livello di installazione impostando il valore specificato dall'argomento.</span><span class="sxs-lookup"><span data-stu-id="21190-104">The SetInstallLevel event changes the installation level to the value specified by the argument.</span></span>

<span data-ttu-id="21190-105">Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="21190-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="21190-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="21190-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="21190-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="21190-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="21190-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="21190-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="21190-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="21190-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="21190-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="21190-110">Published By</span></span>

<span data-ttu-id="21190-111">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="21190-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="21190-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="21190-112">Argument</span></span>

<span data-ttu-id="21190-113">Intero che rappresenta il nuovo valore del livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="21190-113">An integer that is the new value of the installation level.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="21190-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="21190-114">Action on Subscribers</span></span>

<span data-ttu-id="21190-115">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="21190-115">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="21190-116">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="21190-116">Typical Use</span></span>

<span data-ttu-id="21190-117">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per modificare il livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="21190-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to change the installation level.</span></span>

 

 



