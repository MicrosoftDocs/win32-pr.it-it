---
title: Pagina IAgentPropertySheet
description: Pagina IAgentPropertySheet
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711353"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet:: sepage

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Imposta la pagina corrente della finestra delle proprietà di Microsoft Agent.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

BSTR che imposta la pagina corrente della proprietà. Il parametro può essere uno dei seguenti.



|                 |                        |
|-----------------|------------------------|
| **Discorso**    | Pagina di input vocale. |
| **Output**    | Pagina di output.       |
| **Copyright** | Pagina di copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: GetPage**](iagentpropertysheet--getpage.md)


 

 




