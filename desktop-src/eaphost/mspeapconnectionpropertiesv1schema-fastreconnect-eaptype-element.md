---
title: Elemento per riconnessione rapida (EapType)
description: Informazioni sull'elemento per riconnessione rapida (EapType). Questo elemento indica se eseguire una riconnessione rapida.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento per riconnessione rapida EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300438"
---
# <a name="fastreconnect-eaptype-element"></a>Elemento per riconnessione rapida (EapType)

L'elemento **per riconnessione rapida (EapType)** indica se eseguire una riconnessione rapida.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

L'elemento **per riconnessione rapida** è definito dall'elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se l'elemento **per riconnessione rapida** è true, PEAP tenta di eseguire una riconnessione rapida. Se FALSE, PEAP esegue l'autenticazione completa. L'elemento **per riconnessione rapida** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





