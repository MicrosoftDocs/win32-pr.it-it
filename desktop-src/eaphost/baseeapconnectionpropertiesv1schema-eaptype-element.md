---
title: Elemento EapType (proprietà di connessione dello schema v1)
description: Informazioni sull'elemento EapType. Questo elemento acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP. | Elemento EapType (proprietà di connessione dello schema v1)
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
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761662"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Elemento EapType (proprietà di connessione dello schema v1)

L'elemento **EapType** acquisisce la configurazione specifica del metodo all'interno dell'elemento EAP.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Commenti

L'elemento **EapType** è astratto; ogni metodo deve definire e utilizzare un elemento derivato nei documenti dell'istanza.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





