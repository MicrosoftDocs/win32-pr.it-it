---
title: IAgentEx GetVersion
description: IAgentEx GetVersion
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359abb1d22e2cd34fb6b31d85012ac0110f14037
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330855"
---
# <a name="iagentexgetversion"></a>IAgentEx:: GetVersion

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Recupera il numero di versione di Microsoft Agent Server.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

Indirizzo di una variabile che riceve la versione principale.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

Indirizzo di una variabile che riceve la versione secondaria.

</dd> </dl>

 

 




