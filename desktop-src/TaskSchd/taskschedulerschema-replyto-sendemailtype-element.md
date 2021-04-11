---
title: Elemento ReplyTo (sendEmailType)
description: Contiene gli indirizzi di posta elettronica a cui viene risposto nel messaggio di posta elettronica.
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo-elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121555"
---
# <a name="replyto-sendemailtype-element"></a>Elemento ReplyTo (sendEmailType)

Contiene gli indirizzi di posta elettronica a cui viene risposto nel messaggio di posta elettronica.

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

L'elemento **ReplyTo** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà ReplyTo di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).

Per lo sviluppo di script, vedere [**EmailAction. ReplyTo**](emailaction-replyto.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





