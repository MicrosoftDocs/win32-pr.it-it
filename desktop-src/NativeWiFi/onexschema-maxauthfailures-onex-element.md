---
description: Specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Elemento maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9cb48479b2fe26ecb2667812cc6ee2048226c0665c25b12e25e8c7edbc35dac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800781"
---
# <a name="maxauthfailures-onex-element"></a>Elemento maxAuthFailures (OneX)

L'elemento maxAuthFailures (OneX) specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.

Questo elemento è facoltativo. Quando maxAuthFailures non è specificato in un profilo, viene usato un valore pari a uno.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento maxAuthFailures** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




