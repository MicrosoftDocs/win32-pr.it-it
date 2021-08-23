---
title: Scaricamento IAgent
description: Scaricamento IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610141"
---
# <a name="iagentunload"></a>IAgent::UnLoad

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Scarica i dati di tipo carattere per il carattere specificato dalla [**raccolta Characters.**](/windows/desktop/lwef/the-characters-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

ID del carattere.

</dd> </dl>

Usare questo metodo quando non è più necessario un carattere per liberare la memoria usata per archiviare le informazioni sul carattere. Se si accede di nuovo al carattere, usare il [**metodo Load.**](load-method.md)

## <a name="see-also"></a>Vedere anche

[**IAgent::Load**](iagent--load.md)


 

 