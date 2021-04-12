---
title: Elemento Subject (sendEmailType)
description: Contiene l'oggetto del messaggio di posta elettronica.
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Utilità di pianificazione elemento oggetto
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519118"
---
# <a name="subject-sendemailtype-element"></a>Elemento Subject (sendEmailType)

Contiene l'oggetto del messaggio di posta elettronica.

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

L'elemento **Subject** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà Subject di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).

Per lo sviluppo di script, vedere [**EmailAction. Subject**](emailaction-subject.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





