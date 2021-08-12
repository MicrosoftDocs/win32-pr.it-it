---
title: Elemento EapHostUserCredentials
description: Contiene l'elemento EapMethod e l'elemento Credentials o CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Elemento EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a18922ef19bd828067ddb0153aa7c6369ecfeebd0446f5a6481f91fa64ca21b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274421"
---
# <a name="eaphostusercredentials-element"></a>Elemento EapHostUserCredentials

**L'elemento EapHostUserCredentials** contiene l'elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) e [**l'elemento Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) o [**CredentialsBlob.**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md)

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
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



| Elemento                                                                                                | Tipo                                                                                                                | Descrizione                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Credenziali**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Viene usato quando la configurazione del metodo è in formato testo XML anziché in un BLOB binario.<br/>   |
| [**CredenzialiBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | Hexbinary                                                                                                           | Viene usato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifica il metodo a cui si fa riferimento. <br/>                                             |



## <a name="remarks"></a>Commenti

Gli [**elementi Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) [**e CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) non possono essere usati contemporaneamente.

Esiste un punto di estensione per altri spazi dei nomi.

**L'elemento processContents** consente miglioramenti futuri dello schema. **L'elemento processContents** è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





