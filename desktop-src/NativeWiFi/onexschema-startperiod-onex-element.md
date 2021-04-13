---
description: Specifica il tempo di attesa, in secondi, prima dell'invio di un EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Elemento startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345346"
---
# <a name="startperiod-onex-element"></a>Elemento startPeriod (OneX)

L'elemento startPeriod (OneX) specifica il periodo di tempo, in secondi, di attesa prima dell'invio di un EAPOL-Start. Viene inviato un messaggio di EAPOL-Start per avviare il processo di autenticazione 802.1 X.

Questo elemento è facoltativo. Quando startPeriod non viene specificato in un profilo, viene utilizzato un valore di 5 secondi.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="startPeriod">
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

L'elemento **startPeriod** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

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

 

 




