---
description: Specifica il numero di tentativi di pre-autenticazione nei provider di servizi di accesso adiacenti.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8bc310d19126a0e4bc9a7e6abf2a6ae1d0eb917cb5f425796d10bee66ea6ebed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064601"
---
# <a name="preauththrottle-security-element"></a>Elemento preAuthThrottle (security)

L'elemento preAuthThrottle (security) specifica il numero di tentativi di preautenticazione nei provider di servizi di accesso adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode impostato**](wlan-profileschema-pmkcachemode-security-element.md) su "enabled". Se **PMKCacheMode è** abilitato e questo elemento è assente, il numero di tentativi viene impostato su 3 per impostazione predefinita.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="preAuthThrottle"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="16"
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

 

 




