---
title: Elemento UseWinLogonCredentials (EapType)
description: Informazioni sull'elemento UseWinLogonCredentials (EapType). Questo elemento controlla l'uso di credenziali WinLogin.
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
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730370"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>Elemento UseWinLogonCredentials (EapType)

L'elemento **UseWinLogonCredentials (EapType)** controlla l'uso delle credenziali WinLogin.

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

L'elemento **UseWinLogonCredentials** è definito dall'elemento [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Commenti

Se TRUE, EAP MS-CHAPv2 ottiene le credenziali da Winlogon. Se FALSE, EAP MS-CHAPv2 ottiene le credenziali dall'utente. L'elemento **UseWinLogonCredentials (EapType)** è facoltativo.

## <a name="requirements"></a>Requisiti



| Ruolo | Versioni minime del sistema operativo supportate |
|------|-------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



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

 

 





