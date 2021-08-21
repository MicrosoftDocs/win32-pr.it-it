---
description: Specifica lo standard LAN wireless 802.11 utilizzato su una LAN wireless.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (connectivity)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684021"
---
# <a name="phytype-connectivity-element"></a>Elemento phyType (connectivity)

L'elemento phyType (connettività) specifica lo standard LAN wireless 802.11 utilizzato su una LAN wireless.

È possibile specificare **più phyType.** Se non **viene specificato alcun phyType,** il profilo può essere usato per connettersi a qualsiasi **phyType**. Il valore "n" è supportato solo in Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito [**dall'elemento connectivity.**](wlan-profileschema-connectivity-msm-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Connettività**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**connettività (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




