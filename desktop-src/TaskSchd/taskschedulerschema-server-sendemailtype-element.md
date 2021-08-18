---
title: Elemento Server (sendEmailType)
description: Contiene il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Elemento Server Utilità di pianificazione
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6052ebb5e648c040c321a311a6ba18313244ab20340d5a7f6c4185e3d35f5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002249"
---
# <a name="server-sendemailtype-element"></a>Elemento Server (sendEmailType)

Contiene il server di posta elettronica utilizzato per inviare il messaggio di posta elettronica.

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

**L'elemento Server** è definito dal [**tipo complesso sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Server di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server)

Per lo sviluppo di script, [**vedere EmailAction.Server.**](emailaction-server.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





