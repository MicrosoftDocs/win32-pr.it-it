---
description: Specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967404"
---
# <a name="cacheuserdata-onex-element"></a>Elemento cacheUserData (OneX)

L'elemento cacheUserData (OneX) specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive. Quando cacheUserData è TRUE, le credenziali vengono memorizzate nella cache. Quando cacheUserData è FALSE, le credenziali non vengono memorizzate nella cache e all'utente potrebbero essere richieste le credenziali per i successivi tentativi di connessione.

Questo elemento è facoltativo. Quando cacheUserData non viene specificato in un profilo, le credenziali utente vengono memorizzate nella cache.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

L'elemento **cacheUserData** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 




