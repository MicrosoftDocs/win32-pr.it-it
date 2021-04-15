---
description: Specifica il numero di tentativi di pre-autenticazione da provare negli APs adiacenti.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (Security)
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
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525753"
---
# <a name="preauththrottle-security-element"></a>Elemento preAuthThrottle (Security)

L'elemento preAuthThrottle (Security) specifica il numero di tentativi di pre-autenticazione da provare negli APs adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled". Se **PMKCacheMode** è abilitato e questo elemento è assente, il numero di tentativi predefinito è 3.

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

 

 




