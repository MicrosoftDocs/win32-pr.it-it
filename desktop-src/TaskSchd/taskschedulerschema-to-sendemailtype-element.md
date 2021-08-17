---
title: Elemento To (sendEmailType)
description: Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- A elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2367686e308eb33287dafc3ce274d039b71534048fea07bc313e0542af4e2041
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355641"
---
# <a name="to-sendemailtype-element"></a>Elemento To (sendEmailType)

Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.

``` syntax
<xs:element name="To"
    type="string"
 />
```

**L'elemento To** è definito dal tipo complesso [**sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà To di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Per lo sviluppo di script, [**vedere EmailAction.To**](emailaction-to.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





