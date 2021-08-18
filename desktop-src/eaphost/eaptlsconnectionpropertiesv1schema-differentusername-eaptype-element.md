---
title: Elemento DifferentUsername (EapType)
description: Informazioni sull'elemento DifferentUsername (EapType). Questo elemento determina il nome utente che EAP-TLS deve usare.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2980a55e76d238578822cfc8db54a9b6c324e21d4a8f0481ab9bc91e050fb008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984091"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

**L'elemento DifferentUsername (EapType)** determina il nome utente che EAP-TLS deve usare.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

**L'elemento DifferentUsername** è definito dall'elemento [**EapType.**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se **l'elemento DifferentUserName** è TRUE, EAP-TLS deve usare un nome utente diverso da quello visualizzato nel certificato. Se **l'elemento DifferentUserName** è FALSE, EAP-TLS usa il nome utente visualizzato nel certificato.

**L'elemento DifferentUserName** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





