---
description: Contiene le impostazioni di sicurezza per le reti cablate.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685061"
---
# <a name="security-msm-element-lan_policy"></a>Elemento Security (MSM) (LAN_policy)

L'elemento security (MSM) contiene le impostazioni di sicurezza per le reti cablate. Questo elemento è facoltativo.

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

**L'elemento** di sicurezza è definito dall'elemento [**MSM.**](lan-profileschema-msm-lanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo    | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Specifica se il servizio di configurazione automatica per le reti cablate tenterà l'autenticazione delle porte usando 802.1X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Specifica se il servizio di configurazione automatica per le reti cablate richiede l'uso di 802.1X per l'autenticazione delle porte. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




