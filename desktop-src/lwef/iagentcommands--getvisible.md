---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d63ef62a0e57539d633d595901c6cfde1a252ac9ef369f9f56bc3ddaaeea0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961911"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands::GetVisible

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Recupera il valore della proprietà [**Visible**](visible-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Indirizzo di una variabile che riceve il valore della proprietà [**Visible**](visible-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [ **IAgentCommands::SetCaption**](iagentcommands--setcaption.md)


 

 