---
description: Identifica l'APN o la stringa di connessione da utilizzare per stabilire una connessione dati.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307548"
---
# <a name="accessstring-contexttype-element"></a>Elemento AccessString (contextType)

L'elemento **AccessString (ContextType)** identifica l'APN o la stringa di connessione da usare per stabilire una connessione dati.

Questo elemento può avere una lunghezza massima di 100 caratteri.

Questo elemento è facoltativo.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **AccessString** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Contesto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




