---
description: Contiene informazioni sull'autore del profilo.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129570"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Elemento ProfileCreationType (MBNProfile)

L'elemento **ProfileCreationType (MBNProfile)** contiene informazioni sull'autore del profilo.

Questo elemento può avere uno dei valori seguenti.



| Valore                 | Significato                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Questo profilo viene creato dalle informazioni fornite dall'utente del dispositivo.                                                     |
| "AdminProvisioned"    | Questo profilo viene creato dagli amministratori IT e distribuito agli utenti.                                                     |
| "OperatorProvisioned" | Questo profilo viene creato da un operatore di rete e distribuito agli utenti.                                                    |
| "DeviceProvisioned"   | Questo profilo viene creato dal servizio Mobile Broadband usando le informazioni archiviate nel contesto con provisioning del dispositivo. |



 

Si tratta di un elemento facoltativo.

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **ProfileCreationType** è definito dall'elemento [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




