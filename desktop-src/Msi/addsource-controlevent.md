---
description: Questo evento invia una notifica al programma di installazione, mantenendo la finestra di dialogo attualmente in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite dall'origine.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: ControlEvent AddSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7441fb6cdf10abf25798c5e56405b6b4eab11b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311073"
---
# <a name="addsource-controlevent"></a><span data-ttu-id="610e4-103">ControlEvent AddSource</span><span class="sxs-lookup"><span data-stu-id="610e4-103">AddSource ControlEvent</span></span>

<span data-ttu-id="610e4-104">Questo evento invia una notifica al programma di installazione, mantenendo la finestra di dialogo attualmente in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite dall'origine.</span><span class="sxs-lookup"><span data-stu-id="610e4-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run from source.</span></span> <span data-ttu-id="610e4-105">Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="610e4-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="610e4-106">Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="610e4-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="610e4-107">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="610e4-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="610e4-108">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="610e4-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="610e4-109">Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="610e4-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="610e4-110">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="610e4-110">Published By</span></span>

<span data-ttu-id="610e4-111">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="610e4-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="610e4-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="610e4-112">Argument</span></span>

<span data-ttu-id="610e4-113">Stringa, ovvero il nome della funzionalità o "ALL".</span><span class="sxs-lookup"><span data-stu-id="610e4-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="610e4-114">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="610e4-114">Action on Subscribers</span></span>

<span data-ttu-id="610e4-115">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="610e4-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="610e4-116">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="610e4-116">Typical Use</span></span>

<span data-ttu-id="610e4-117">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e utilizzato per notificare al programma di installazione senza arrestare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="610e4-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



