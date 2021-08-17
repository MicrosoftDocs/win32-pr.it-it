---
title: Elemento Username (TLS)
description: Informazioni sull'elemento Username. Questo elemento acquisisce il nome utente da inviare nella EAP-Identity risposta.
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
ms.openlocfilehash: 6748ac8c352540d2288cf3bf3c790004d832ba47961fbc7b9e8211fa712ccb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117720120"
---
# <a name="username-element-tls"></a>Elemento Username (TLS)

**L'elemento Username** acquisisce il nome utente da inviare nella EAP-Identity risposta.

Se **l'elemento Username** è assente, EAP-TLS usa il nome nel certificato a cui si fa riferimento [**nell'elemento UserCert.**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md)

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a>Requisiti



| Ruolo | Versioni minime supportate del sistema operativo |
|------|-------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





