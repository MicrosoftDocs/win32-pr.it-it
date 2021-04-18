---
title: Tipo complesso BaseEapParameters-proprietà di connessione
description: Definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.
ms.assetid: 510debce-545c-4ce1-965b-e4b2185b7983
keywords:
- BaseEapParameters di tipo complesso EAPHost
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
ms.openlocfilehash: f3bfb9f6c833900967525467202421cf94166405
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323809"
---
# <a name="baseeapparameters-complex-type---connection-properties"></a>Tipo complesso BaseEapParameters-proprietà di connessione

Il tipo complesso **BaseEapParameters** definisce l'elemento segnaposto per il tipo di metodo e la configurazione specifica del metodo.

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
| [**Type**](baseeapconnectionpropertiesv1schema-type-baseeapparameters-element.md) | numero intero | Qualsiasi istanza dello schema è consentita in questo punto.<br/> |



## <a name="remarks"></a>Commenti

In **BaseEapParameters** il metodo può definire gli elementi costitutivi. Il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





