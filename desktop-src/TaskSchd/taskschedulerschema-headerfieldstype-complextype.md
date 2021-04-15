---
title: Tipo complesso headerFieldsType
description: Definisce gli elementi che specificano i campi per un'intestazione di posta elettronica.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- Utilità di pianificazione di tipo complesso headerFieldsType
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475964"
---
# <a name="headerfieldstype-complex-type"></a>Tipo complesso headerFieldsType

Definisce gli elementi che specificano i campi per un'intestazione di posta elettronica.

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                                       | Descrizione                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Specifica un campo in un'intestazione di messaggio di posta elettronica. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





