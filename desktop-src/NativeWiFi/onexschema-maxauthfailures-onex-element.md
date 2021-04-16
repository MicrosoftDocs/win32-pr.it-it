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
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529029"
---
# <a name="maxauthfailures-onex-element"></a>Elemento maxAuthFailures (OneX)

L'elemento maxAuthFailures (OneX) specifica il numero massimo di errori di autenticazione consentiti per un set di credenziali.

Questo elemento è facoltativo. Quando maxAuthFailures non viene specificato in un profilo, viene utilizzato un valore di uno.

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

L'elemento **maxAuthFailures** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**OneX**](onexschema-onex-element.md)
</dt> </dl>

 

 




