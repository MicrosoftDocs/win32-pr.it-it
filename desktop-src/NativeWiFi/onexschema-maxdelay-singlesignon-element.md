---
description: Specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-on abbia esito negativo.
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
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881457"
---
# <a name="maxdelay-singlesignon-element"></a>Elemento maxDelay (singleSignOn)

L'elemento maxDelay (singleSignOn) specifica, in secondi, il ritardo massimo prima che il tentativo di connessione Single Sign-on abbia esito negativo.

Questo elemento è facoltativo. Quando maxDelay non viene specificato in un profilo, viene utilizzato un valore di 10 secondi.

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

L'elemento **maxDelay** è definito dall'elemento [**singleSignOn**](onexschema-singlesignon-onex-element.md) .

## <a name="remarks"></a>Commenti

Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** . Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 
