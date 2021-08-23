---
description: Specifica il periodo di tempo, in secondi, durante il quale un client non tenterà nuovamente l'autenticazione dopo un tentativo di autenticazione non riuscito.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Elemento heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5a2009ac8518d114353e3323b97c4ea57c54fc801447c375641b8f6bbd1b2bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684852"
---
# <a name="heldperiod-onex-element"></a>Elemento heldPeriod (OneX)

L'elemento heldPeriod (OneX) specifica l'intervallo di tempo, in secondi, durante il quale un client non tenterà nuovamente l'autenticazione dopo un tentativo di autenticazione non riuscito.

Questo elemento è facoltativo. Se heldPeriod non è specificato in un profilo, viene usato un valore di 1 secondo.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento heldPeriod** è definito dall'elemento [**OneX.**](onexschema-onex-element.md)

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

 

 




