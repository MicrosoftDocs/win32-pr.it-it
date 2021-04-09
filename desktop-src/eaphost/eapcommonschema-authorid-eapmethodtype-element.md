---
title: Elemento autorizzato (EapMethodType)
description: Informazioni sull'elemento autorizzato (EapMethodType). L'elemento autorizzato (EapMethodType) si riferisce all'autore del metodo.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento autorizzato EAPHost
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
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963466"
---
# <a name="authorid-eapmethodtype-element"></a>Elemento autorizzato (EapMethodType)

L'elemento autorizzato **(EapMethodType)** si riferisce all'autore del metodo.

L'autorizzazione è un numero univoco emesso da IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

L'elemento **autorizzato** è definito dal tipo complesso [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Commenti

Gli elementi **autorizzazioned** e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.

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

 

 





