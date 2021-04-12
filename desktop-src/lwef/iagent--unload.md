---
title: Scaricamento IAgent
description: Scaricamento IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337359"
---
# <a name="iagentunload"></a>IAgent:: UnLoad

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Scarica i dati di tipo carattere per il carattere specificato dalla raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

ID del carattere.

</dd> </dl>

Utilizzare questo metodo quando non è più necessario un carattere, per liberare memoria utilizzata per archiviare le informazioni sul carattere. Se si accede di nuovo al carattere, utilizzare il metodo [**Load**](load-method.md) .

## <a name="see-also"></a>Vedere anche

[**IAgent:: Load**](iagent--load.md)


 

 