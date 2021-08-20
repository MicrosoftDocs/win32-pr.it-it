---
title: Tipo complesso BaseEapParameters - Proprietà di connessione
description: Definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- Tipo complesso BaseEapParameters EAPHost
topic_type:
- apiref
api_name:
- BaseEapParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ae3abf23b19badb123f8eb49097c6b3e9d7ac6d26fc0132f34b84de5ac24c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086955"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Tipo complesso BaseEapParameters - Proprietà di connessione

Il **tipo complesso BaseEapParameters** definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.

``` syntax
<xs:complexType name="BaseEapParameters">
    <xs:sequence>
        <xs:element name="Type"
            type="integer"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo    | Descrizione                                     |
|------------------------------------------------------------------------------------|---------|-------------------------------------------------|
| [**Type**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | numero intero | Qualsiasi istanza dello schema è consentita qui.<br/> |



## <a name="remarks"></a>Commenti

In **BaseEapParameters il** metodo può definire gli elementi costitutivi. Il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





