---
title: Elemento AuthorId (EapMethodType)
description: Informazioni sull'elemento AuthorId (EapMethodType). L'elemento AuthorID (EapMethodType) fa riferimento all'autore del metodo.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento AuthorId EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021751"
---
# <a name="authorid-eapmethodtype-element"></a>Elemento AuthorId (EapMethodType)

**L'elemento AuthorId (EapMethodType)** fa riferimento all'autore del metodo.

AuthorId è un numero univoco emesso dall'autorità IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

**L'elemento AuthorId** è definito dal tipo complesso [**EapMethodType.**](eapcommonschema-eapmethodtype-complextype.md)

## <a name="remarks"></a>Commenti

Gli **elementi AuthorId** [**e VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



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

 

 





