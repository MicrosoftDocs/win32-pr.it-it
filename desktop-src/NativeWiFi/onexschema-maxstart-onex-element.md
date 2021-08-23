---
description: Specifica il numero massimo di EAPOL-Start inviati.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Elemento maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7c50945b8de53b6d058556e3b5c995d3ec17bfdc8f8d55ec3dc2e6e56089b2a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800761"
---
# <a name="maxstart-onex-element"></a>Elemento maxStart (OneX)

L'elemento maxStart (OneX) specifica il numero massimo di EAPOL-Start inviati. Dopo l'invio EAPOL-Start numero massimo di messaggi, il client presuppone che nella rete non sia presente alcun autenticatore.

Questo elemento è facoltativo. Quando maxStart non è specificato in un profilo, viene usato un valore di 3 messaggi.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="maxStart">
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

**L'elemento maxStart** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




