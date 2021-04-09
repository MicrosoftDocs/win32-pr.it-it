---
title: GetGuid IAgentCharacterEx
description: GetGuid IAgentCharacterEx
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e0e14d0931774bf6ab5e1c8599bbebaadd0ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955673"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx:: GetGuid

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Recupera l'ID univoco per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

Indirizzo di un BSTR che riceve l'ID per il carattere.

</dd> </dl>

La proprietà restituisce una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) utilizzata dal server per identificare in modo univoco il carattere. Quando viene compilato con l'editor dei caratteri di Microsoft Agent, viene impostato un identificatore di caratteri. la proprietà è di sola lettura.

 

 




