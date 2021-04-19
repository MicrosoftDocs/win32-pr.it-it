---
description: Panoramica della visualizzazione del pannello input.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Visualizzazione del pannello input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319575"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="ecb8a-103">Visualizzazione del pannello input</span><span class="sxs-lookup"><span data-stu-id="ecb8a-103">Displaying the Input Panel</span></span>

<span data-ttu-id="ecb8a-104">\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) per il codice gestito).</span><span class="sxs-lookup"><span data-stu-id="ecb8a-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="ecb8a-105">Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]</span><span class="sxs-lookup"><span data-stu-id="ecb8a-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="ecb8a-106">Di seguito è riportato l'ordine dei vari eventi di stato attivo per un controllo:</span><span class="sxs-lookup"><span data-stu-id="ecb8a-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="ecb8a-107">Controllo. invio</span><span class="sxs-lookup"><span data-stu-id="ecb8a-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="ecb8a-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="ecb8a-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="ecb8a-109">Controllo. Leave</span><span class="sxs-lookup"><span data-stu-id="ecb8a-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="ecb8a-110">Controllo. convalida</span><span class="sxs-lookup"><span data-stu-id="ecb8a-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="ecb8a-111">Controllo. convalidato</span><span class="sxs-lookup"><span data-stu-id="ecb8a-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="ecb8a-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="ecb8a-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="ecb8a-113">Non vi è alcuna garanzia che il controllo abbia lo stato attivo nel momento in cui la proprietà [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) viene scritta quando è impostata nel gestore eventi [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="ecb8a-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="ecb8a-114">L'evento Control. Enter è il posto migliore per l'associazione dell'oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un controllo, ma l'evento [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) è il posto migliore per modificare la proprietà [PenInputPanel. Visible](/previous-versions/ms571984(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="ecb8a-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
