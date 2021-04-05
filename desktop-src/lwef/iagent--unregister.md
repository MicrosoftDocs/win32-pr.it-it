---
title: Annullare la registrazione di IAgent
description: Annullare la registrazione di IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872509"
---
# <a name="iagentunregister"></a>IAgent:: Annulla registrazione

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Scarica i dati di tipo carattere per il carattere specificato dalla raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

ID sink di notifica.

</dd> </dl>

Utilizzare questo metodo quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione viene arrestata.

## <a name="see-also"></a>Vedere anche

[**IAgent:: Register**](iagent--register.md)


 

 