---
title: Elemento VendorId (EapMethodType)
description: Fa riferimento al fornitore che ha definito il metodo se l'elemento Type (EapMethodType) è 254 (un metodo EAP espanso).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29508121a9724a52df19038b82d97576a924c3c8bab49ac6801c1de51ec71919
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067301"
---
# <a name="vendorid-eapmethodtype-element"></a>Elemento VendorId (EapMethodType)

**L'elemento VendorId (EapMethodType)** fa riferimento al fornitore che ha definito il metodo se l'elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso).

**VendorId è** facoltativo. Se usato, **VendorId è** un numero univoco emesso da Internet Assigned Numbers Authority (IANA).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

**L'elemento VendorId** è definito dal tipo complesso [**EapMethodType.**](eapcommonschema-eapmethodtype-complextype.md)

## <a name="remarks"></a>Commenti

Gli [**elementi AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) **e VendorId** non devono essere uguali per un metodo specifico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



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

 

 





