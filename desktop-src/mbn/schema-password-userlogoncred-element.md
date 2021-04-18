---
description: Specifica la password utilizzata per autenticare un utente.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (UserLogonCred)-elemento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306778"
---
# <a name="password-userlogoncred-element"></a>Password (UserLogonCred)-elemento

L'elemento [**password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) specifica la password usata per autenticare un utente.

L'elemento è una stringa composta da un massimo di 255 caratteri.

Questo elemento è facoltativo.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

L'elemento **password** è definito dall'elemento [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .

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

 

 




