---
title: Elemento Ccn (sendEmailType)
description: Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- Utilità di pianificazione elemento Ccn
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120218"
---
# <a name="bcc-sendemailtype-element"></a>Elemento Ccn (sendEmailType)

Contiene gli indirizzi di posta elettronica utilizzati nella riga Ccn di un messaggio di posta elettronica.

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

L'elemento **Ccn** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà Ccn di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).

Per lo sviluppo di script, vedere [**EmailAction. Ccn**](emailaction-bcc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





