---
title: Registro IAgent
description: Registro IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856241"
---
# <a name="iagentregister"></a>IAgent:: Register

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registra un sink di notifica per l'applicazione client.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Indirizzo di [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) per l'interfaccia del sink di notifica.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Indirizzo dell'ID sink di notifica (utilizzato per annullare la registrazione del sink di notifica).

</dd> </dl>

Per ricevere gli eventi dal server Microsoft Agent, è necessario registrare il sink di notifica (noto anche come sink di notifica o sink di evento).

## <a name="see-also"></a>Vedere anche

[**IAgent:: Annulla registrazione**](iagent--unregister.md)


 

 




