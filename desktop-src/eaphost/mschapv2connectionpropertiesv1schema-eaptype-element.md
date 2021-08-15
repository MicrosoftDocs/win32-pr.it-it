---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: Tipo derivato dell'elemento EapType dallo schema baseeapconnectionpropertiesv1. Si tratta dell'elemento principale visualizzato all'interno dell'elemento Config dello schema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18d3296dfab4a28ba818199d0b9329888c692f55831bced2af5abedfd1f205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984061"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Elemento EapType (mschapv2connectionpropertiesv1schema)

**L'elemento EapType** è un tipo derivato dell'elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) dallo schema [baseeapconnectionpropertiesv1.](baseeapconnectionpropertiesv1schema-schema.md) Si tratta dell'elemento principale visualizzato all'interno dell'elemento Config dello schema [EapHostConfig](eaphostconfigschema-elements.md)

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                       | Tipo    | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | Controlla l'uso delle credenziali winlogin. Se TRUE, il MS-CHAPv2 EAP ottiene le credenziali da winlogon. Se FALSE, il MS-CHAPv2 EAP ottiene le credenziali dall'utente. <br/> [**L'elemento UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) è facoltativo.<br/> |



## <a name="remarks"></a>Commenti

**L'elemento processContents** consente miglioramenti futuri allo schema. **L'elemento processContents** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





