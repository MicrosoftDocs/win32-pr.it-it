---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica che EAP-TLS deve leggere il certificato dall'archivio personale dell'utente o dal computer in fase di autenticazione.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518333"
---
# <a name="certificatestore-credentialssourceparameters-element"></a>Elemento CertificateStore (CredentialsSourceParameters)

L'elemento **CertificateStore (CredentialsSourceParameters)** indica che EAP-TLS deve leggere il certificato dall'archivio personale dell'utente o dal computer in fase di autenticazione.

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

L'elemento **CertificateStore** è definito dal tipo complesso [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .

## <a name="remarks"></a>Commenti

Gli elementi **CertificateStore** e [**smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) non possono essere usati contemporaneamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**CredentialsSource (EapType)**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





