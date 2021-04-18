---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298015"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow:: GetVisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Determina se la finestra dei comandi vocali è visibile o nascosta.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se la finestra dei comandi vocali è visibile oppure **false** se nascosta.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow:: sevisible**](iagentcommandwindow--setvisible.md)


 

 




