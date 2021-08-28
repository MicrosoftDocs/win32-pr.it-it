---
title: Elemento HeaderFields (sendEmailType)
description: Specifica i campi di intestazione e i relativi valori utilizzati nell'intestazione del messaggio di posta elettronica.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Elemento HeaderFields Utilità di pianificazione
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2af801385c74fa26221556b713faf8db915037ef4cf7439d71a2e2d4004193d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100031"
---
# <a name="headerfields-sendemailtype-element"></a>Elemento HeaderFields (sendEmailType)

Specifica i campi di intestazione e i relativi valori utilizzati nell'intestazione del messaggio di posta elettronica.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

**L'elemento HeaderFields** è definito dal [**tipo complesso sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                                       | Descrizione                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Contiene un campo per un'intestazione in un messaggio di posta elettronica. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà HeaderFields di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)

Per lo sviluppo di script, [**vedere EmailAction.HeaderFields.**](emailaction-headerfields.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





