---
title: Elemento SimpleCertSelection (CertSelection)
description: Informazioni sull'elemento SimpleCertSelection (CertSelection). Questo elemento determina il modo in cui l'utente seleziona un certificato.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047373"
---
# <a name="simplecertselection-certselection-element"></a>Elemento SimpleCertSelection (CertSelection)

L'elemento **SimpleCertSelection (CertSelection)** determina il modo in cui l'utente seleziona un certificato.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

L'elemento **SimpleCertSelection** è definito dal tipo complesso [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .

## <a name="remarks"></a>Commenti

Per impostazione predefinita, **SimpleCertSelection** è true. Se **SimpleCertSelection** è true, EAP-TLS esegue una semplice ricerca di certificati senza elenchi a discesa per la selezione dei certificati. Se **SimpleCertSelection** è false, EAP-TLS illustra all'utente il certificato appropriato da selezionare.

## <a name="requirements"></a>Requisiti



| Ruolo | Sistema operativo minimo supportato |
|------|----------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**CertificateStore (CredentialsSourceParameters)**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





