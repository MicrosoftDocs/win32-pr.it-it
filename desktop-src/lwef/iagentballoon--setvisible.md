---
title: IAgentBalloon visibile
description: IAgentBalloon visibile
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298265"
---
# <a name="iagentballoonsetvisible"></a>IAgentBalloon:: sevisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

Imposta la proprietà [**Visible**](visible-property.md) per la parola Balloon.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Impostazione della proprietà Visible. Il valore **true** Visualizza la parola Balloon; il valore **false** lo nasconde.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon:: GetVisible**](iagentballoon--getvisible.md)


 

 




