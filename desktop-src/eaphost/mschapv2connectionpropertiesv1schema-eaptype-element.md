---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: È un tipo derivato dell'elemento EapType dello schema baseeapconnectionpropertiesv1. Si tratta dell'elemento principale che viene visualizzato all'interno dell'elemento config dello schema EapHostConfig.
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334318"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Elemento EapType (mschapv2connectionpropertiesv1schema)

L'elemento **EapType** è un tipo derivato dell'elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) dello schema [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) . Si tratta dell'elemento principale visualizzato all'interno dell'elemento config dello schema [EapHostConfig](eaphostconfigschema-elements.md)

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
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | boolean | Controlla l'uso delle credenziali WinLogin. Se TRUE, EAP MS-CHAPv2 ottiene le credenziali da Winlogon. Se FALSE, EAP MS-CHAPv2 ottiene le credenziali dall'utente. <br/> L'elemento [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) è facoltativo.<br/> |



## <a name="remarks"></a>Commenti

L'elemento **processContents** consente miglioramenti futuri allo schema. L'elemento **processContents** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





