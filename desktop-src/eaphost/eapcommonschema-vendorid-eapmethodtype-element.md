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
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517890"
---
# <a name="vendorid-eapmethodtype-element"></a>Elemento VendorId (EapMethodType)

L'elemento **VendorID (EapMethodType)** fa riferimento al fornitore che ha definito il metodo se l'elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso).

**VendorID** è facoltativo. Se usato, **VendorID** è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

L'elemento **VendorID** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Commenti

Gli elementi [**autorizzazioned**](eapcommonschema-authorid-eapmethodtype-element.md) e **VendorID** non devono essere uguali per un metodo specifico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 





