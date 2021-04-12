---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396126"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet:: GetPage

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Recupera la pagina corrente della finestra delle proprietà di Microsoft Agent.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Indirizzo di una variabile che riceve la pagina corrente della finestra delle proprietà (ultima pagina visualizzata se la finestra non è aperta). Il parametro può essere uno dei seguenti:



|                 |                        |
|-----------------|------------------------|
| **Discorso**    | Pagina di input vocale. |
| **Output**    | Pagina di output.       |
| **Copyright** | Pagina di copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: sepage**](iagentpropertysheet--setpage.md)


 

 




