---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749825"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands::GetCount

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Recupera il numero di [**oggetti Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Indirizzo di una variabile che riceve il numero di [**comandi**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

*pdwCount* include solo il numero [**di comandi**](/windows/desktop/lwef/the-command-object) definiti nella raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Le voci del server o di altre voci client non sono incluse.

 

 