---
title: Tipo complesso CertSelection
description: Informazioni sul tipo complesso CertSelection. Questo tipo determina il modo in cui l'utente seleziona un certificato.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Tipo complesso CertSelection EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 375ea26fddf07f8d775617c0a2167ed02aa8160de8cc5dde49a92f37f57a335e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984131"
---
# <a name="certselection-complex-type"></a>Tipo complesso CertSelection

Il **tipo complesso CertSelection** determina il modo in cui l'utente seleziona un certificato.

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                     | Tipo    | Descrizione                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | boolean | È TRUE per impostazione predefinita. Se [**SimpleCertSelection è**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) TRUE, EAP-TLS esegue una semplice ricerca di certificati senza elenchi a discesa per la selezione dei certificati. Se **SimpleCertSelection** è FALSE, EAP-TLS indica all'utente il certificato appropriato da selezionare.<br/> |



## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Tipi complessi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





