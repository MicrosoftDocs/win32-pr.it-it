---
description: Il ControlEvent DoAction notifica al programma di installazione di eseguire un'azione personalizzata. Questo evento può essere pubblicato tramite un controllo pulsante, un controllo CheckBox o un controllo SelectionTree. Questo evento deve essere creato nella tabella ControlEvent.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent DoAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128387"
---
# <a name="doaction-controlevent"></a><span data-ttu-id="cca53-105">ControlEvent DoAction</span><span class="sxs-lookup"><span data-stu-id="cca53-105">DoAction ControlEvent</span></span>

<span data-ttu-id="cca53-106">Il ControlEvent DoAction notifica al programma di installazione di eseguire un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="cca53-106">The DoAction ControlEvent notifies the installer to execute a custom action.</span></span> <span data-ttu-id="cca53-107">Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md) , un controllo [CheckBox](checkbox-control.md) o un controllo [SelectionTree](selectiontree-control.md) .</span><span class="sxs-lookup"><span data-stu-id="cca53-107">This event can be published by a [PushButton](pushbutton-control.md) control, [CheckBox](checkbox-control.md) control, or a [SelectionTree](selectiontree-control.md) control.</span></span> <span data-ttu-id="cca53-108">Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cca53-108">This event should be authored into the [ControlEvent](controlevent-table.md) table.</span></span>

<span data-ttu-id="cca53-109">Si noti che le azioni personalizzate avviate da un ControlEvent DoAction possono inviare un messaggio con il [**metodo del messaggio**](session-message.md), ma non possono inviare un messaggio con [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="cca53-109">Note that custom actions launched by a DoAction ControlEvent can send a message with the [**Message Method**](session-message.md), but cannot send a message with [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="cca53-110">Nei sistemi precedenti a Windows Server 2003, le azioni personalizzate avviate da un DoAction ControlEvent non possono inviare messaggi con **MsiProcessMessage** o **Metodo Message**.</span><span class="sxs-lookup"><span data-stu-id="cca53-110">On systems prior to Windows Server 2003, custom actions launched by a DoAction ControlEvent cannot send messages with **MsiProcessMessage** or **Message Method**.</span></span> <span data-ttu-id="cca53-111">Per altre informazioni, vedere [invio di messaggi a Windows Installer con MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="cca53-111">For more information, see [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="cca53-112">Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cca53-112">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="cca53-113">Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cca53-113">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="cca53-114">Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cca53-114">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="cca53-115">Pubblicato da</span><span class="sxs-lookup"><span data-stu-id="cca53-115">Published By</span></span>

<span data-ttu-id="cca53-116">Questo ControlEvent viene pubblicato dal programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="cca53-116">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="cca53-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="cca53-117">Argument</span></span>

<span data-ttu-id="cca53-118">Stringa, il nome dell'azione personalizzata da eseguire.</span><span class="sxs-lookup"><span data-stu-id="cca53-118">A string, the name of the custom action to be executed.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="cca53-119">Azione sui sottoscrittori</span><span class="sxs-lookup"><span data-stu-id="cca53-119">Action on Subscribers</span></span>

<span data-ttu-id="cca53-120">Questo ControlEvent non esegue un'azione sui sottoscrittori.</span><span class="sxs-lookup"><span data-stu-id="cca53-120">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="cca53-121">Utilizzo tipico</span><span class="sxs-lookup"><span data-stu-id="cca53-121">Typical Use</span></span>

<span data-ttu-id="cca53-122">Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per richiamare un'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="cca53-122">A [PushButton](pushbutton-control.md) control on a dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to invoke a custom action.</span></span>

 

 



