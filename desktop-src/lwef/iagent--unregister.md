---
title: Annullamento della registrazione di IAgent
description: Annullamento della registrazione di IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976481"
---
# <a name="iagentunregister"></a>IAgent::Unregister

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Scarica i dati di tipo carattere per il carattere specificato dalla [**raccolta Characters.**](/windows/desktop/lwef/the-characters-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

ID del sink di notifica.

</dd> </dl>

Usare questo metodo quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione viene arrestata.

## <a name="see-also"></a>Vedere anche

[**IAgent::Register**](iagent--register.md)


 

 