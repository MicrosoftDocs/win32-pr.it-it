---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949591bc22c93711af19ce18cb024ede9714335f249839eb4819a73e231e0d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976241"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow::GetVisible

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Determina se la finestra Comandi vocali è visibile o nascosta.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** la finestra Comandi vocali è visibile o **False** se nascosta.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow::SetVisible**](iagentcommandwindow--setvisible.md)


 

 




