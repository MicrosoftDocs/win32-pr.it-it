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
ms.openlocfilehash: ddf3e70607cedbaed45da19651ec73736a54bfafab197e95d2cd634d8e3833f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959841"
---
# <a name="profilecreationtype-mbnprofile-element"></a>Elemento ProfileCreationType (MBNProfile)

**L'elemento ProfileCreationType (MBNProfile)** contiene informazioni sull'autore del profilo.

Questo elemento può avere uno dei valori seguenti.



| Valore                 | Significato                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| "UserProvisioned"     | Questo profilo viene creato dalle informazioni fornite dall'utente del dispositivo.                                                     |
| "AdminProvisioned"    | Questo profilo viene creato dagli amministratori IT e distribuito agli utenti.                                                     |
| "OperatorProvisioned" | Questo profilo viene creato da un operatore di rete e distribuito agli utenti.                                                    |
| "DeviceProvisioned"   | Questo profilo viene creato dal servizio Mobile Broadband usando le informazioni archiviate nel contesto di provisioning del dispositivo. |



 

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

**L'elemento ProfileCreationType** è definito dall'elemento [**MBNProfile.**](schema-mbnprofile-element.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




