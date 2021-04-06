---
title: Elemento UserCert (EapType)
description: Si riferisce all'hash SHA-1 del certificato che deve essere utilizzato per l'autenticazione.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Elemento UserCert EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743199"
---
# <a name="usercert-eaptype-element"></a>Elemento UserCert (EapType)

L'elemento **userCert (EapType)** si riferisce all'hash SHA-1 del certificato che deve essere usato per l'autenticazione.

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

L'elemento **userCert** è definito dall'elemento [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





