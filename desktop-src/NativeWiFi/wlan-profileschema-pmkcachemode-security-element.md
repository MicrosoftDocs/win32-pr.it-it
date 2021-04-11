---
description: Indica se verrà utilizzata la memorizzazione nella cache PMK.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 609660d6f3161cbaaa5e0505daf9c6b9180b6c32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128847"
---
# <a name="pmkcachemode-security-element"></a>Elemento PMKCacheMode (Security)

L'elemento PMKCacheMode (Security) indica se verrà utilizzata la memorizzazione nella cache di PMK. Questo elemento è valido solo per le reti definite da WPA2. La memorizzazione nella cache PMK è descritta nella specifica [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**sicurezza**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




