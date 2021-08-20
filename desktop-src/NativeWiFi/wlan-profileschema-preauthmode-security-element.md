---
description: Indica se la pre-autenticazione verrà utilizzata dal client.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Elemento preAuthMode (security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dd8fad733b66337572b428ad9b15bbf8e24fb96444a646100a331f7ec9ce460a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797789"
---
# <a name="preauthmode-security-element"></a>Elemento preAuthMode (security)

L'elemento preAuthMode (security) indica se la preautententura verrà usata dal client. La pre-autenticazione è necessaria per il roaming rapido sicuro WPA2. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode impostato**](wlan-profileschema-pmkcachemode-security-element.md) su "enabled". Se **PMKCacheMode è** abilitato e questo elemento è assente, il valore predefinito è "disabled".

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="preAuthMode"
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

L'elemento è definito [**dall'elemento di**](wlan-profileschema-security-msm-element.md) sicurezza .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Sicurezza**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




