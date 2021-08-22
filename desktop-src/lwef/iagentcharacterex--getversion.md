---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864bd0cf53e9dd94a547a459bb17cd477189401d544aebca047ead2f049c1c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750474"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx::GetVersion

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Recupera il numero di versione del set di animazioni standard dei caratteri.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

Indirizzo di una variabile che riceve la versione principale.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

Indirizzo di una variabile che riceve la versione secondaria.

</dd> </dl>

Il numero di versione del set di animazioni standard viene impostato automaticamente quando lo si compila con l'editor di caratteri di Microsoft Agent.

 

 




