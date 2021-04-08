---
title: Elemento User
description: Informazioni sull'elemento User. Questo elemento non viene usato quando si usano i metodi legacy tramite le API EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento utente EAPHost
topic_type:
- apiref
api_name:
- User
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b564b6f91244a6839bc256dcdb2f79c630a4b065
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730362"
---
# <a name="user-element"></a>Elemento User

L'elemento **User** non viene usato quando si usano i metodi legacy tramite le API EAPHost.

``` syntax
<xs:element name="User">
    <xs:complexType>
        <xs:sequence>
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                  | Tipo | Descrizione                                                                     |
|----------------------------------------------------------|------|---------------------------------------------------------------------------------|
| [**EAP**](baseeapuserpropertiesv1schema-eap-element.md) |      | Acquisisce le informazioni sulle credenziali specifiche del metodo e del tipo di metodo.<br/> |



## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima del sistema operativo supportata |
|------|------------------------------|
| Client<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





