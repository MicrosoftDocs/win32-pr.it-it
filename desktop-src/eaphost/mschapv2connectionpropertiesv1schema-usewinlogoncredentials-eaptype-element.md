---
title: Elemento UseWinLogonCredentials (EapType)
description: Informazioni sull'elemento UseWinLogonCredentials (EapType). Questo elemento controlla l'uso delle credenziali winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Elemento UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2a407c505139562a155e5aa9d7ed57fed5d15077cf5d035ea8bb7bbe0e177363
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086192"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

**L'elemento UseWinLogonCredentials (EapType)** controlla l'uso delle credenziali winlogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

**L'elemento UseWinLogonCredentials** è definito dall'elemento [**EapType.**](mschapv2connectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Commenti

Se TRUE, il MS-CHAPv2 EAP ottiene le credenziali da winlogon. Se FALSE, il MS-CHAPv2 EAP ottiene le credenziali dall'utente. **L'elemento UseWinLogonCredentials (EapType)** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versioni minime supportate del sistema operativo |
|------|-------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





