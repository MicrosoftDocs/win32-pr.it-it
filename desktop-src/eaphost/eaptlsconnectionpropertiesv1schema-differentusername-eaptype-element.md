---
title: Elemento DifferentUsername (EapType)
description: Informazioni sull'elemento DifferentUsername (EapType). Questo elemento determina il nome utente EAP-TLS da usare.
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
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300476"
---
# <a name="differentusername-eaptype-element"></a>Elemento DifferentUsername (EapType)

L'elemento **DifferentUsername (EapType)** determina il nome utente EAP-TLS da usare.

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

L'elemento **DifferentUsername** è definito dall'elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se l'elemento **DifferentUserName** è true, EAP-TLS deve usare un nome utente diverso dal nome visualizzato nel certificato. Se l'elemento **DifferentUserName** è false, EAP-TLS usa il nome utente visualizzato nel certificato.

L'elemento **DifferentUserName** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





