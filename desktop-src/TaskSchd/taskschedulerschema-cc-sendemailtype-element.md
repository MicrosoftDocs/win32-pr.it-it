---
title: Elemento CC (sendEmailType)
description: Contiene gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Utilità di pianificazione elemento CC
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477794"
---
# <a name="cc-sendemailtype-element"></a>Elemento CC (sendEmailType)

Contiene gli indirizzi di posta elettronica usati nella riga CC di un messaggio di posta elettronica.

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

L'elemento **CC** è definito dal tipo complesso [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà CC di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).

Per lo sviluppo di script, vedere [**EmailAction.CC**](emailaction-cc.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





