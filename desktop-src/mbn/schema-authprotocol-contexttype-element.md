---
description: Specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).
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
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306781"
---
# <a name="authprotocol-contexttype-element"></a>Elemento AuthProtocol (contextType)

L'elemento **AuthProtocol (ContextType)** specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).

L'elemento può avere uno dei valori seguenti.

| Valore      | Significato                                                                 |
|------------|-------------------------------------------------------------------------|
| NESSUNO     | Nessun protocollo di autenticazione.                                             |
| PAP      | Autenticazione della password non crittografata.                                    |
| CHAP     | Challenge Handshake Authentication Protocol (CHAP).                      |
|  MsCHAPV2 | Usare Microsoft Challenge Handshake Authentication Protocol (CHAP) v 2.0. |



 

Questo elemento è facoltativo e viene usato solo per i profili GSM. Se l'elemento non è specificato e il profilo è per un dispositivo GSM, il servizio Mobile Broadband userà **"None"**.

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

L'elemento **AuthProtocol** è definito dal tipo complesso [**contextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**Contesto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




