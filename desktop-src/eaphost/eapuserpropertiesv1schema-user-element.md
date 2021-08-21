---
title: Elemento User
description: Informazioni sull'elemento User. Questo elemento non viene usato quando si usano metodi legacy tramite le API EAPHost.
ms.assetid: d35fb4ba-5f48-431d-b2bf-738043f5d1ff
keywords:
- Elemento User EAPHost
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
ms.openlocfilehash: d0f21b22320029bf1d10a209eae6a3b2192512a541c1e681b71e112d488c87ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086405"
---
# <a name="user-element"></a>Elemento User

**L'elemento User** non viene usato quando si usano metodi legacy tramite le API EAPHost.

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
| [**Eap**](baseeapuserpropertiesv1schema-eap-element.md) |      | Acquisisce le informazioni sulle credenziali specifiche del metodo e del tipo di metodo.<br/> |



## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





