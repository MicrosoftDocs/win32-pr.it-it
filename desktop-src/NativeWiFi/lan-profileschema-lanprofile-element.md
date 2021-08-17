---
description: Contiene un profilo di rete cablata.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Elemento LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6adaa0f4884ad275137a6c949dbc466416006f33bb6603dc61e87153d9b23361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065101"
---
# <a name="lanprofile-element"></a>Elemento LANProfile

L'elemento LANProfile contiene un profilo di rete cablata. Questo elemento è l'elemento radice univoco per un profilo di rete cablata.

Lo spazio dei nomi di destinazione per l'elemento LANProfile è `https://www.microsoft.com/networking/LAN/profile/v1` .

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
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

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo    | Descrizione                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSM**](lan-profileschema-msm-lanprofile-element.md)                 |         | Contiene le impostazioni del modulo MSM (Media Specific Module). <br/>                                                                               |
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | boolean | Specifica se il servizio di configurazione automatica per le reti cablate tenterà l'autenticazione della porta tramite 802.1X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | boolean | Specifica se il servizio di configurazione automatica per le reti cablate richiede l'uso di 802.1X per l'autenticazione delle porte. <br/> |
| [**Sicurezza**](lan-profileschema-security-msm-element.md)              |         | Contiene le impostazioni di sicurezza. <br/>                                                                                                  |



## <a name="remarks"></a>Commenti

Per visualizzare l'elenco degli elementi figlio in una struttura ad albero, vedere Elementi dello [ \_ schema del profilo LAN.](lan-profileschema-elements.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




