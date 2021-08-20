---
description: Contiene un oggetto hexBinary a 3 byte che identifica l'IHV.
ms.assetid: 0b2e73fb-df3a-48c4-b38d-970c37de46eb
title: Elemento OUI (OUIHeader)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUI
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ae1ed2481da09a9ab34c62b592860b1b3b8be35d2d8da3a86676f00bb880210b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797901"
---
# <a name="oui-ouiheader-element"></a>Elemento OUI (OUIHeader)

L'elemento OUI (OUIHeader) contiene un elemento hexBinary a 3 byte che identifica l'IHV.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="OUI">
    <xs:simpleType>
        <xs:restriction
            base="hexBinary"
        >
            <xs:length
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito [**dall'elemento OUIHeader.**](wlan-profileschema-ouiheader-ihv-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
</dt> </dl>

 

 




