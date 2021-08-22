---
title: Elemento FastReconnect (EapType)
description: Informazioni sull'elemento FastReconnect (EapType). Questo elemento indica se eseguire una riconnessione rapida.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento FastReconnect EAPHost
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
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238721"
---
# <a name="fastreconnect-eaptype-element"></a>Elemento FastReconnect (EapType)

**L'elemento FastReconnect (EapType)** indica se eseguire una riconnessione rapida.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

**L'elemento FastReconnect** è definito dall'elemento [**EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se **l'elemento FastReconnect** è TRUE, PEAP tenta di eseguire una riconnessione rapida. se FALSE, PEAP esegue l'autenticazione completa. **L'elemento FastReconnect** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementi dello schema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





