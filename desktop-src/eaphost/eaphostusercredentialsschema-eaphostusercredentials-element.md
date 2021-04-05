---
title: Elemento EapHostUserCredentials
description: Contiene l'elemento EapMethod e le credenziali o l'elemento CredentialsBlob.
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
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120566"
---
# <a name="eaphostusercredentials-element"></a>Elemento EapHostUserCredentials

L'elemento **EapHostUserCredentials** contiene l'elemento [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) e le [**credenziali**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) o l'elemento [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .

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
| [**Credenziali**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [**BaseEapMethodUserCredentials**](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | Viene usato quando la configurazione del metodo è in formato testo XML anziché come BLOB binario.<br/>   |
| [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | hexBinary                                                                                                           | Viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.<br/> |
| [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)                                                  | Identifica il metodo a cui si fa riferimento. <br/>                                             |



## <a name="remarks"></a>Commenti

Gli elementi [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) non possono essere usati contemporaneamente.

Esiste un punto di estensione per altri spazi dei nomi.

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

[Schema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





