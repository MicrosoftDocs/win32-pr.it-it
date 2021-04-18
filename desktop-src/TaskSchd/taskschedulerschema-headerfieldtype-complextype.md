---
title: Tipo complesso headerFieldType
description: Definisce gli elementi utilizzati per creare un campo di intestazione in un messaggio di posta elettronica.
ms.assetid: 66036875-1116-46eb-b2f5-8c8ad8373ab1
keywords:
- Utilità di pianificazione di tipo complesso headerFieldType
topic_type:
- apiref
api_name:
- headerFieldType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ddbc0ae22c6baf3fd288cbe2ead19dac506afee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301334"
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





