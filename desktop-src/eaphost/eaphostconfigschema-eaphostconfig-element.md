---
title: Elemento EapHostConfig
description: Contiene l'elemento EapMethod e la configurazione o l'elemento ConfigBlob. Gli elementi config e ConfigBlob non possono essere usati contemporaneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Elemento EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047786"
---
# <a name="eaphostconfig-element"></a>Elemento EapHostConfig

L'elemento **EapHostConfig** contiene l'elemento [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) e l'elemento [**config**](eaphostconfigschema-config-eaphostconfig-element.md) o [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .

Gli elementi [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) non possono essere usati contemporaneamente.

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
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



| Elemento                                                                    | Tipo                                                                                     | Descrizione                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**File di configurazione**](eaphostconfigschema-config-eaphostconfig-element.md)         | [**BaseEapMethodConfig**](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.<br/>       |
| [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) | hexBinary                                                                                | Viene usato quando la configurazione del metodo è in formato BLOB binario anziché in formato testo stringa.<br/> |
| [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                       | Identifica il metodo a cui si fa riferimento. <br/>                                                 |



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

[Schema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





