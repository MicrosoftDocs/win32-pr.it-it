---
description: Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-On non riesca.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: cd4e82e8031f57e9672dd11a066a9a1fb2e8f3540c93dc4e1898afa4f1cf6302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684841"
---
# <a name="maxdelay-singlesignon-element"></a>Elemento maxDelay (singleSignOn)

L'elemento maxDelay (singleSignOn) specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-On non riesca.

Questo elemento è facoltativo. Quando maxDelay non è specificato in un profilo, viene usato un valore di 10 secondi.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**L'elemento maxDelay** è definito dall'elemento [**singleSignOn.**](onexschema-singlesignon-onex-element.md)

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando usando il **comando netsh wlan set profileparameter.** Per altre informazioni, vedere [Comandi Netsh per la rete locale wireless (wlan).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**singleSignOn**](onexschema-singlesignon-onex-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
