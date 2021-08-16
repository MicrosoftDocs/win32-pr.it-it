---
title: Elemento Bcc (sendEmailType)
description: Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Elemento Bcc Utilità di pianificazione
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1409d50a0317758534724b9e2c3a9796c4dd0cb40e666f58fc65ca0771da9762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659041"
---
# <a name="bcc-sendemailtype-element"></a>Elemento Bcc (sendEmailType)

Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

**L'elemento Bcc** è definito dal tipo complesso [**sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Bcc di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc)

Per lo sviluppo di script, [**vedere EmailAction.Bcc.**](emailaction-bcc.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





