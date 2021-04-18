---
title: Elemento to (sendEmailType)
description: Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- All'elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301145"
---
# <a name="to-sendemailtype-element"></a>Elemento to (sendEmailType)

Contiene gli indirizzi di posta elettronica a cui verrà inviato il messaggio di posta elettronica.

``` syntax
<xs:element name="To"
    type="string"
 />
```

L'elemento **to** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**to property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).

Per lo sviluppo di script, vedere [**EmailAction.to**](emailaction-to.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





