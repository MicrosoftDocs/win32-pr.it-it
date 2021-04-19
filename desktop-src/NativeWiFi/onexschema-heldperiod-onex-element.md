---
description: Specifica l'intervallo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.
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
ms.openlocfilehash: f8664543a9ea5b0f3b290168129e589e9ccd68ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311674"
---
# <a name="heldperiod-onex-element"></a>Elemento heldPeriod (OneX)

L'elemento heldPeriod (OneX) specifica il periodo di tempo, in secondi, in cui un client non tenterà di nuovo l'autenticazione dopo un tentativo di autenticazione non riuscito.

Questo elemento è facoltativo. Quando heldPeriod non viene specificato in un profilo, viene utilizzato un valore di 1 secondo.

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

L'elemento **heldPeriod** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

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

 

 




