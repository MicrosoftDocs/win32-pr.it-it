---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf67c3ecb10ec5a8372a00e11d356e4b050b50be4a0563d9c4ebeefcd8040f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476791"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Imposta la pagina corrente della finestra delle proprietà di Microsoft Agent.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

Oggetto BSTR che imposta la pagina corrente della proprietà. Il parametro può essere uno dei seguenti.



|                 | Descrizione            |
|-----------------|------------------------|
| **"Voce"**    | Pagina Input vocale. |
| **"Output"**    | Pagina Output.       |
| **"Copyright"** | Pagina Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




