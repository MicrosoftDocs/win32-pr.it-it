---
title: Elemento Body (sendEmailType)
description: Contiene il testo nel corpo del messaggio di posta elettronica.
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Utilità di pianificazione elemento Body
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301907"
---
# <a name="body-sendemailtype-element"></a>Elemento Body (sendEmailType)

Contiene il testo nel corpo del messaggio di posta elettronica.

``` syntax
<xs:element name="Body"
    type="string"
 />
```

L'elemento **Body** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà Body di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).

Per lo sviluppo di script, vedere [**EmailAction. Body**](emailaction-body.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





