---
title: Password (EapType)-elemento
description: Informazioni sull'elemento password (EapType). Questo elemento identifica la password dell'utente o del computer da autenticare.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Elemento password EAPHost
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
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047378"
---
# <a name="password-eaptype-element"></a>Password (EapType)-elemento

L'elemento **password (EapType)** identifica la password dell'utente o del computer da autenticare.

``` syntax
<xs:element name="Password"
    type="string"
 />
```

L'elemento **password** è definito dall'elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se l'elemento **password (EapType)** non è presente, l'hash della password viene ottenuto da Winlogon. Questo elemento è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 





