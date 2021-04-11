---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: Viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.
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
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119343"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>Elemento CredentialsBlob (EapHostUserCredentials)

L'elemento **CredentialsBlob (EapHostUserCredentials)** viene utilizzato quando la configurazione del metodo è un BLOB binario anziché in formato testo XML.

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

L'elemento **CredentialsBlob** è definito dall'elemento [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .

## <a name="remarks"></a>Commenti

Gli elementi [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) e **CredentialsBlob** non possono essere usati contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 





