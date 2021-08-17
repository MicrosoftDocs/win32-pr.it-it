---
description: Contiene le impostazioni del modulo MSM (Media Specific Module).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 25334050e95ff20cf35ed1071bf2b1c006e29c0f9374923199a96c09bbae0471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065081"
---
# <a name="msm-lanprofile-element"></a>Elemento MSM (LANProfile)

L'elemento MSM (LANProfile) contiene le impostazioni del modulo MSM (Media Specific Module).

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

**L'elemento MSM** è definito dall'elemento [**LANProfile.**](lan-profileschema-lanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo    | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Specifica se il servizio di configurazione automatica per le reti cablate tenterà l'autenticazione della porta tramite 802.1X.<br/>       |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Specifica se il servizio di configurazione automatica per le reti cablate richiede l'uso di 802.1X per l'autenticazione delle porte. <br/> |
| [**Sicurezza**](lan-profileschema-security-msm-element.md)              |         | Contiene le impostazioni di sicurezza. <br/>                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**PROFILO LAN**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**PROFILO LAN**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




