---
description: Specifica il protocollo di autenticazione da usare per attivare un contesto PDP (Packet Data Protocol).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 65b944b2966c9b5cac307f6f8efe6af2f42a1ffa5b4f2f400074caa0efe9f84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975260"
---
# <a name="authprotocol-contexttype-element"></a>Elemento AuthProtocol (contextType)

**L'elemento AuthProtocol (contextType)** specifica il protocollo di autenticazione da usare per attivare un contesto PDP (Packet Data Protocol).

L'elemento può avere uno dei valori seguenti.

| Valore      | Significato                                                                 |
|------------|-------------------------------------------------------------------------|
| "NONE"     | Nessun protocollo di autenticazione.                                             |
| "PAP"      | Autenticazione con password non crittografata.                                    |
| "CHAP"     | Challenge Handshake Authentication Protocol (CHAP).                      |
|  MsCHAPV2" | Usare Microsoft Challenge Handshake Authentication Protocol (CHAP) v2.0. |



 

Questo elemento è facoltativo e viene usato solo per i profili GSM. Se l'elemento non è specificato e il profilo è per un dispositivo GSM, il servizio Mobile Broadband userà **"NONE".**

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento AuthProtocol** è definito dal [**tipo complesso contextType.**](schema-contexttype-complextype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Contexttype**](schema-contexttype-complextype.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**Contesto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




