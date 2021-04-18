---
description: Specifica la modalità di gestione delle password durante l'aggiornamento dei profili.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Elemento IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307535"
---
# <a name="ignorepassword-userlogoncred-element"></a>Elemento IgnorePassword (UserLogonCred)

L'elemento **IgnorePassword (UserLogonCred)** specifica come gestire le password quando si aggiornano i profili.

Se è impostato su **true** e un profilo con lo stesso nome esiste al momento dell'operazione di aggiornamento, la password del profilo verrà acquisita e archiviata nel nuovo profilo.

Questo elemento è facoltativo.

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

L'elemento **IgnorePassword** è definito dall'elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**UserLogonCred**](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**UserLogonCred (contextType)**](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




