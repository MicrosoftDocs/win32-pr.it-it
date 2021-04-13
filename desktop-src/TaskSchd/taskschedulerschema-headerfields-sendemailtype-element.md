---
title: Elemento HeaderFields (sendEmailType)
description: Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- Utilità di pianificazione elemento HeaderFields
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518190"
---
# <a name="headerfields-sendemailtype-element"></a>Elemento HeaderFields (sendEmailType)

Specifica i campi di intestazione e i relativi valori usati nell'intestazione del messaggio di posta elettronica.

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

L'elemento **HeaderFields** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                                       | Descrizione                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [**HeaderField**](taskschedulerschema-headerfield-headerfieldstype-element.md) | [**headerFieldType**](taskschedulerschema-headerfieldtype-complextype.md) | Contiene un campo per un'intestazione in un messaggio di posta elettronica. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà HeaderFields di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).

Per lo sviluppo di script, vedere [**EmailAction. HeaderFields**](emailaction-headerfields.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





