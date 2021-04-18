---
title: Elemento UserName (TLS)
description: Informazioni sull'elemento UserName. Questo elemento acquisisce il nome utente da inviare nella risposta EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Elemento Username EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300480"
---
# <a name="username-element-tls"></a>Elemento UserName (TLS)

L'elemento **username** acquisisce il nome utente da inviare nella risposta EAP-Identity.

Se l'elemento **username** è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento nell'elemento [**userCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Requisiti



| Ruolo | Versioni minime del sistema operativo supportate |
|------|-------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





