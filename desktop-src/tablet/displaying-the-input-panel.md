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
# <a name="displaying-the-input-panel"></a>Visualizzazione del pannello input

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) per il codice gestito). Vedere la pagina relativa alla [programmazione del pannello input di testo](programming-the-text-input-panel.md).\]

Di seguito è riportato l'ordine dei vari eventi di stato attivo per un controllo:

-   [Controllo. invio](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Controllo. Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Controllo. convalida](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Controllo. convalidato](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control. LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Non vi è alcuna garanzia che il controllo abbia lo stato attivo nel momento in cui la proprietà [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) viene scritta quando è impostata nel gestore eventi [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) . L'evento Control. Enter è il posto migliore per l'associazione dell'oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un controllo, ma l'evento [Control. GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) è il posto migliore per modificare la proprietà [PenInputPanel. Visible](/previous-versions/ms571984(v=vs.100)) .

 

 
