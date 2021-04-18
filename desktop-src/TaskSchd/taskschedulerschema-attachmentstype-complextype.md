---
title: Tipo complesso attachmentsType
description: Definisce gli elementi utilizzati per specificare un allegato inviato con un messaggio di posta elettronica.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- Utilità di pianificazione di tipo complesso attachmentsType
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302172"
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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





