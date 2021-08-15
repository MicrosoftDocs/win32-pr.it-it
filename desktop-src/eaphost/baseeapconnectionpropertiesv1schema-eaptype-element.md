---
title: Elemento EapType (proprietà di connessione dello schema v1)
description: Informazioni sull'elemento EapType. Questo elemento acquisisce la configurazione specifica del metodo all'interno dell'elemento Eap. | Elemento EapType (proprietà di connessione dello schema v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f2681e5682ad98ab5f4185174996920315d8c3b81dde8ba69d13ca178904ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498787"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Elemento EapType (proprietà di connessione dello schema v1)

**L'elemento EapType** acquisisce la configurazione specifica del metodo all'interno dell'elemento Eap.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Commenti

**L'elemento EapType** è astratto. ogni metodo deve definire e usare un elemento derivato nei documenti dell'istanza.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





