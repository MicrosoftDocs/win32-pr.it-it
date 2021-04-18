---
title: Tipo complesso BaseEapParameters-proprietà utente
description: Definisce l'elemento che ha specificato il metodo legacy selezionato e le credenziali specifiche del metodo.
ms.assetid: bc42e536-f741-4821-8453-6c0631daad3e
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
ms.openlocfilehash: 451c03123634dd98a1f4a49292db0a807009f6f5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323771"
---
# <a name="baseeapparameters-complex-type---user-properties"></a>Tipo complesso BaseEapParameters-proprietà utente

Il tipo complesso **BaseEapParameters** definisce l'elemento che ha specificato il metodo legacy selezionato e le credenziali specifiche del metodo.

Il metodo può definire gli elementi costitutivi all'interno di **BaseEapParameters**; il metodo esegue anche la convalida dello schema sugli elementi in **BaseEapParameters**.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





