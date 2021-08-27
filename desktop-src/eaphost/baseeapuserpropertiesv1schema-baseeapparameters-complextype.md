---
title: Tipo complesso BaseEapParameters - Proprietà utente
description: Definisce l'elemento che specifica il metodo legacy selezionato e le credenziali specifiche del metodo.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 80ae1dc749d1c31ee11809b530fe1b04a59ce3e4e4dc76e84323b7dc078ec44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978291"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Tipo complesso BaseEapParameters - Proprietà utente

Il **tipo complesso BaseEapParameters** definisce l'elemento che specifica il metodo legacy selezionato e le credenziali specifiche del metodo.

Il metodo può definire gli elementi costitutivi **all'interno di BaseEapParameters;** Il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters.**

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



| Elemento                                                                      | Tipo    | Descrizione                                                                                               |
|------------------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------|
| [**Type**](baseeapuserpropertiesv1schema-type-baseeapparameters-element.md) | numero intero | Definisce l'elemento segnaposto per il tipo di metodo selezionato e le credenziali specifiche del metodo. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Schema EAPHost e legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





