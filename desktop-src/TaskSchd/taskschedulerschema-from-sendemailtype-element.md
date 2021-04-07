---
title: Elemento from (sendEmailType)
description: Contiene l'indirizzo di posta elettronica del mittente del messaggio di posta elettronica.
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- Da elemento Utilità di pianificazione
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048150"
---
# <a name="from-sendemailtype-element"></a>Elemento from (sendEmailType)

Contiene l'indirizzo di posta elettronica del mittente del messaggio di posta elettronica.

``` syntax
<xs:element name="From"
    type="string"
 />
```

L'elemento **from** viene definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere la [**Proprietà from di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).

Per lo sviluppo di script, vedere [**EmailAction. from**](emailaction-from.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





