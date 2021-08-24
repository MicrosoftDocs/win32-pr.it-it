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
ms.openlocfilehash: d7f4663153fa9aff176180387ebaf0321ab3d48ec2c382e9e84c0f524d6e0ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800871"
---
# <a name="cacheuserdata-onex-element"></a>Elemento cacheUserData (OneX)

L'elemento cacheUserData (OneX) specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive. Quando cacheUserData è TRUE, le credenziali vengono memorizzate nella cache. Quando cacheUserData è FALSE, le credenziali non vengono memorizzate nella cache e all'utente potrebbero essere richieste le credenziali nei tentativi di connessione successivi.

Questo elemento è facoltativo. Quando cacheUserData non è specificato in un profilo, le credenziali utente vengono memorizzate nella cache.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

**L'elemento cacheUserData** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




