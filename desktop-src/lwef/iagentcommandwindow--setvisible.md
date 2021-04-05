---
title: IAgentCommandWindow visibile
description: IAgentCommandWindow visibile
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044910"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow:: sevisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Impostare la proprietà [**Visible**](visible-property.md) per la finestra dei comandi vocali.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Impostazione della proprietà [**Visible**](visible-property.md) . Il valore **true** Visualizza la finestra comandi vocali; **False** lo nasconde.

</dd> </dl>

L'utente può eseguire l'override di questa proprietà.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandWindow:: GetVisible**](iagentcommandwindow--getvisible.md)


 

 




