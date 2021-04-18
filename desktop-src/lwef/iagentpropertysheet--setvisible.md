---
title: IAgentPropertySheet visibile
description: IAgentPropertySheet visibile
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298325"
---
# <a name="iagentpropertysheetsetvisible"></a>IAgentPropertySheet:: sevisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

Imposta la proprietà [**Visible**](visible-property.md) per la finestra delle proprietà di Microsoft Agent.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Impostazione della proprietà Visible. Il valore **true** Visualizza la finestra delle proprietà. il valore **false** lo nasconde.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: GetVisible**](iagentpropertysheet--getvisible.md)


 

 




