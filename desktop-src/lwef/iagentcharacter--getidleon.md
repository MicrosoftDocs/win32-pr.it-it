---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a5ce64b39b615325a3de55c1643004cffaeecf89e2e0a024d317bb56e32d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478370"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indica lo stato di elaborazione inattiva automatica per un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** il server Microsoft Agent riproduce automaticamente le animazioni di stato **idling** per un carattere e **False** in caso contrario.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




