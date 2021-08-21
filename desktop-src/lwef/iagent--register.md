---
title: Registro IAgent
description: Registro IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962671"
---
# <a name="iagentregister"></a>IAgent::Register

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Registra un sink di notifica per l'applicazione client.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Indirizzo di [**IUnknown per l'interfaccia**](https://www.bing.com/search?q=**IUnknown**) del sink di notifica.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*
</dt> <dd>

Indirizzo dell'ID sink di notifica (usato per annullare la registrazione del sink di notifica).

</dd> </dl>

È necessario registrare il sink di notifica (noto anche come sink di notifica o sink di evento) per ricevere eventi dal server Microsoft Agent.

## <a name="see-also"></a>Vedere anche

[**IAgent::Unregister**](iagent--unregister.md)


 

 




