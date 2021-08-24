---
description: Specifica quando viene eseguito l'accesso Single Sign-On.
ms.assetid: 23a7ab31-b29d-4f45-a384-bb2d2c18230f
title: Elemento type (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- type
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a8a395a5cdbd21bd33012e624f069d9447204cc96ffd2996a138ebf5d65f7bb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800731"
---
# <a name="type-singlesignon-element"></a>Elemento type (singleSignOn)

L'elemento type (singleSignOn) specifica quando viene eseguito l'accesso Single Sign-On. Se impostato su `preLogon` , l'accesso Single Sign-On viene eseguito prima dell'accesso dell'utente. Se impostato su `postLogon` , l'accesso Single Sign-On viene eseguito immediatamente dopo l'accesso dell'utente.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="type"
    minOccurs="1"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="preLogon"
             />
            <xs:enumeration
                value="postLogon"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento** type è definito dall'elemento [**singleSignOn.**](onexschema-singlesignon-onex-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 




