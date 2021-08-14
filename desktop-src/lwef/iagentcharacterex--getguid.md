---
title: IAgentCharacterEx GetGUID
description: IAgentCharacterEx GetGUID
ms.assetid: 25fb2531-a81c-4add-8134-77b1cd57cfe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e43a98617b1e2d25a25167ad5b95462eeb462f40f5a353b5a5ec45ffb3a9cca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477969"
---
# <a name="iagentcharacterexgetguid"></a>IAgentCharacterEx::GetGUID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetGUID(
   BSTR * pbszGUID  // address of character's ID
);
```

Recupera l'ID univoco per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszGUID"></span><span id="pbszguid"></span><span id="PBSZGUID"></span>*pbszGUID*
</dt> <dd>

Indirizzo di un BSTR che riceve l'ID per il carattere.

</dd> </dl>

La proprietà restituisce una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) utilizzato dal server per identificare in modo univoco il carattere. Un identificatore di carattere viene impostato quando viene compilato con l'editor di caratteri di Microsoft Agent. la proprietà è di sola lettura.

 

 




