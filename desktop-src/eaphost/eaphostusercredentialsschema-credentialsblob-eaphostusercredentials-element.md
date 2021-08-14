---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: Viene usato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e56fe90677d0988420a97510da75ea24bf9d50610f9b0b06555a127ef5f731c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274475"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Elemento CredentialsBlob (EapHostUserCredentials)

**L'elemento CredentialsBlob (EapHostUserCredentials)** viene usato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

**L'elemento CredentialsBlob** è definito dall'elemento [**EapHostUserCredentials.**](eaphostusercredentialsschema-eaphostusercredentials-element.md)

## <a name="remarks"></a>Commenti

Gli [**elementi Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) **e CredentialsBlob** non possono essere usati contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaphostusercredentials](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





