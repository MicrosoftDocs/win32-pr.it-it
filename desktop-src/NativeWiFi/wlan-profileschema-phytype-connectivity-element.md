---
description: Specifica lo standard LAN wireless 802,11 usato in una LAN wireless.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (Connectivity)
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
ms.openlocfilehash: 71a58e464528136244cec745aed2e59c6fea737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306487"
---
# <a name="phytype-connectivity-element"></a>Elemento phyType (Connectivity)

L'elemento phyType (Connectivity) specifica lo standard della LAN wireless 802,11 usato in una LAN wireless.

È possibile specificare più **phyType** s. Se non viene specificato alcun **phyType** , il profilo può essere usato per connettersi a qualsiasi **phyType**. Il valore "n" è supportato solo in Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.

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

L'elemento è definito dall'elemento [**Connectivity**](wlan-profileschema-connectivity-msm-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**connettività**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**connettività (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




