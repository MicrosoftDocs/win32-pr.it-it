---
title: Tipo complesso attachmentsType
description: Definisce gli elementi utilizzati per specificare un allegato inviato con un messaggio di posta elettronica.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- Tipi complessi attachmentsType Utilità di pianificazione
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d98b266fcb15fbd47fbb2a5bb792b95e4fb765a48b2fbcf6c1185aad9475df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772391"
---
# <a name="attachmentstype-complex-type"></a>Tipo complesso attachmentsType

Definisce gli elementi utilizzati per specificare un allegato inviato con un messaggio di posta elettronica.

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                          | Tipo                                                                    | Descrizione                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**File**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica il percorso di un file inviato come allegato in un messaggio di posta elettronica.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





