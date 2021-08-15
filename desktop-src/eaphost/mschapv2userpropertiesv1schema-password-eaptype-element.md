---
title: Elemento Password (EapType)
description: Informazioni sull'elemento Password (EapType). Questo elemento identifica la password dell'utente o del computer da autenticare.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento Password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbbcb7b0acd372bbe71ee6d22f44a736948b145378f62f40820e3de53d77b875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118273200"
---
# <a name="password-eaptype-element"></a>Elemento Password (EapType)

**L'elemento Password (EapType)** identifica la password dell'utente o del computer da autenticare.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

**L'elemento Password** è definito dall'elemento [**EapType.**](mschapv2userpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se **l'elemento Password (EapType)** non è presente, l'hash della password viene ottenuto da winlogon. Questo elemento è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





