---
title: Tipo complesso BaseEapMethodConfig
description: Informazioni sul tipo complesso BaseEapMethodConfig. Questo tipo è un elemento segnaposto per la configurazione del metodo.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- Tipo complesso BaseEapMethodConfig EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8decb1746391c1337440eb475a8a8face3f8b7466b73015db48e3991841a3c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086776"
---
# <a name="baseeapmethodconfig-complex-type"></a>Tipo complesso BaseEapMethodConfig

Il **tipo complesso BaseEapMethodConfig** è un elemento segnaposto per la configurazione del metodo.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Commenti

Il metodo EAP esegue la convalida dello schema sul contenuto **dell'elemento BaseEapMethodConfig.**

## <a name="requirements"></a>Requisiti



| Ruolo | Versione minima supportata del sistema operativo |
|------|------------------------------|
| Client<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





