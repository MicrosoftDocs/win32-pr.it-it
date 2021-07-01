---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120746"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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


 

 




