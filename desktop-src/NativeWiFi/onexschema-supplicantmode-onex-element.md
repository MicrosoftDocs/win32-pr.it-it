---
description: Specifica il metodo di trasmissione utilizzato per EAPOL-Start messaggi.
ms.assetid: 8d49d19a-8122-4191-bb46-92a2016bcfee
title: Elemento supplicantMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- supplicantMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33d58bd247a220ca93ed4d2a05886be107afd4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311665"
---
# <a name="supplicantmode-onex-element"></a>Elemento supplicantMode (OneX)

L'elemento supplicantMode (OneX) specifica il metodo di trasmissione utilizzato per EAPOL-Start messaggi. Nella tabella seguente sono descritti i valori possibili.



| Valore               | Descrizione                                                                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| inhibitTransmission | EAPOL-Start messaggi non vengono trasmessi. Valido solo per i profili LAN cablati.                                                                                             |
| includeLearning     | Il client determina quando inviare pacchetti di EAPOL-Start in base alla funzionalità di rete. EAPOL-Start messaggi vengono inviati solo quando richiesto. Valido solo per i profili LAN cablati. |
| compliant           | EAPOL-Start messaggi vengono trasmessi come specificato da 802.1 X. Valido per i profili LAN cablati e wireless.                                                             |



 

Questo elemento è facoltativo. Quando supplicantMode non viene specificato in un profilo, viene utilizzato un valore di `compliant` per i profili LAN cablati e wireless.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.

``` syntax
<xs:element name="supplicantMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="inhibitTransmission"
             />
            <xs:enumeration
                value="includeLearning"
             />
            <xs:enumeration
                value="compliant"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento **supplicantMode** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .

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

 

 




