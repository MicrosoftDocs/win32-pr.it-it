---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939026026e18e550ca18838977f00a8878db9039595d9eadd0b30b88235a0248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962321"
---
# <a name="iagentballoongetvisible"></a>IAgentBalloon::GetVisible

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Determina se il fumetto della parola è visibile o nascosto.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve **True** se il fumetto della parola è visibile e **False** se nascosto.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentBalloon::SetVisible**](iagentballoon--setvisible.md)


 

 




