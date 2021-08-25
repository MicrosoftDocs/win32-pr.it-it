---
description: Panoramica della visualizzazione del pannello di input.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Visualizzazione del Pannello input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f491a8b2ddcea42588c38f7cfa7106a2e8f48ff1849ab8cd406718511a4cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940791"
---
# <a name="displaying-the-input-panel"></a>Visualizzazione del Pannello input penna

\[[**PenInputPanel è**](peninputpanel-class.md) stato sostituito [**da TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) per il codice gestito). Fare riferimento a Programmazione [del pannello di input di testo](programming-the-text-input-panel.md).\]

L'ordine dei vari eventi dello stato attivo per un controllo è il seguente:

-   [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [Control.Leave](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [Control.Validating](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [Control.Validated](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [Control.LostFocus](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

Non è garantito che il controllo abbia effettivamente lo stato attivo quando la [proprietà Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) viene scritta quando viene impostata nel gestore dell'evento [Control.Enter.](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) L'evento Control.Enter è la posizione migliore per associare l'oggetto [PenInputPanel](/previous-versions/ms583923(v=vs.100)) a un controllo, ma l'evento [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) è la posizione migliore per modificare la [proprietà PenInputPanel.Visible.](/previous-versions/ms571984(v=vs.100))

 

 
