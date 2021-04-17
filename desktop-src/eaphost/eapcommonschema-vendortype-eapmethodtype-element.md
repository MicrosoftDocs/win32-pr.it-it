---
title: Elemento VendorType (EapMethodType)
description: Informazioni sull'elemento VendorType (EapMethodType). Questo elemento è il tipo definito dal fornitore per il metodo.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorType EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474219"
---
# <a name="vendortype-eapmethodtype-element"></a>Elemento VendorType (EapMethodType)

L'elemento **VendorType (EapMethodType)** è il tipo definito dal fornitore per il metodo.

L'elemento **VendorType** è facoltativo. Se usato, **VendorType** è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

L'elemento **VendorType** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





