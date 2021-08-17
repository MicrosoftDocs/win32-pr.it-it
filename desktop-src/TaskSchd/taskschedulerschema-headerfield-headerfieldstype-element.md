---
title: Elemento HeaderField (headerFieldsType)
description: Contiene un campo per un'intestazione in un messaggio di posta elettronica.
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- Elemento HeaderField Utilità di pianificazione
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918e432ce7a8ea2d43769b9d9ee1315a4b35bce6f2c0cb23f1153ec7afe1a599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139214"
---
# <a name="headerfield-headerfieldstype-element"></a>Elemento HeaderField (headerFieldsType)

Contiene un campo per un'intestazione in un messaggio di posta elettronica.

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

**L'elemento HeaderField** è definito dal [**tipo complesso headerFieldsType.**](taskschedulerschema-headerfieldstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                        | Derivato da                                                                 | Descrizione                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Specifica i campi di intestazione e i relativi valori utilizzati nell'intestazione del messaggio di posta elettronica.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                            | Tipo                                                                    | Descrizione                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Nome**](taskschedulerschema-name-headerfieldtype-element.md)   | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica il nome del campo di intestazione in un messaggio di posta elettronica.<br/> |
| [**Valore**](taskschedulerschema-value-headerfieldtype-element.md) | **string**                                                              | Specifica il valore di un campo di intestazione in un messaggio di posta elettronica.<br/>  |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà HeaderFields di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Per lo sviluppo di script, [**vedere EmailAction.HeaderFields.**](emailaction-headerfields.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





