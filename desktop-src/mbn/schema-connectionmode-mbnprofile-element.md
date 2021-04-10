---
description: Specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: Elemento ConnectionMode (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966661"
---
# <a name="connectionmode-mbnprofile-element"></a>Elemento ConnectionMode (MBNProfile)

L'elemento **ConnectionMode (MBNProfile)** specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.

Questo elemento può avere uno dei valori seguenti.



| Valore       | Significato                                                                |
|-------------|------------------------------------------------------------------------|
| manuale    | Non connettersi mai automaticamente alla rete.                            |
| auto      | Connettersi sempre automaticamente alla rete.                           |
| "auto-Home" | Connettersi automaticamente alla rete tranne che in una rete in roaming. |



 

Questo elemento può avere un massimo di un'occorrenza.

Questo elemento è obbligatorio.

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **ConnectionMode** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




