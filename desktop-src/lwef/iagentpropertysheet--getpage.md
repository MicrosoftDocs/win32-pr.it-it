---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119866"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet::GetPage

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Recupera la pagina corrente della finestra delle proprietà di Microsoft Agent.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Indirizzo di una variabile che riceve la pagina corrente della finestra delle proprietà (ultima pagina visualizzata se la finestra non è aperta). Il parametro può essere uno dei seguenti:



|                 | Descrizione            |
|-----------------|------------------------|
| **"Voce"**    | Pagina Input vocale. |
| **"Output"**    | Pagina Output.       |
| **"Copyright"** | Pagina Copyright.    |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet::SetPage**](iagentpropertysheet--setpage.md)


 

 




