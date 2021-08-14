---
title: Tipo complesso headerFieldType
description: Definisce gli elementi utilizzati per creare un campo di intestazione in un messaggio di posta elettronica.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Tipo complesso headerFieldType Utilità di pianificazione
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78c4fb3a8ca85cea5b765fc1fc4521f968efd76e9169613dc4a1565a43ee1b36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131830"
---
# <a name="headerfieldtype-complex-type"></a>Tipo complesso headerFieldType

Definisce gli elementi utilizzati per creare un campo di intestazione in un messaggio di posta elettronica.

``` syntax
<xs:complexType name="headerFieldType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
         />
        <xs:element name="Value"
            type="string"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                            | Tipo                                                                    | Descrizione                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nome**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica il nome del campo di intestazione in un messaggio di posta elettronica.<br/> |
| [**Valore**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Specifica il valore di un campo di intestazione in un messaggio di posta elettronica.<br/>  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





