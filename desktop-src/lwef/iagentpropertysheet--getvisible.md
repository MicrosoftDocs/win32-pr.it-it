---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330348"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet:: GetVisible

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Determina se la finestra delle proprietà di Microsoft Agent è visibile o nascosta.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se la finestra delle proprietà è visibile e **false** se nascosta.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentPropertySheet:: sevisible**](iagentpropertysheet--setvisible.md)


 

 




