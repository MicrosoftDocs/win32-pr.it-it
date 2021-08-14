---
title: Elemento Attachments (sendEmailType)
description: Contiene un elenco di allegati nel messaggio di posta elettronica.
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- Elemento Attachments Utilità di pianificazione
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8aa87679c6d6db725c26deee817fe04acacca85e39d3a8f75c04cba9680ea846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132066"
---
# <a name="attachments-sendemailtype-element"></a>Elemento Attachments (sendEmailType)

Contiene un elenco di allegati nel messaggio di posta elettronica.

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

**L'elemento Attachments** è definito dal [**tipo complesso sendEmailType.**](taskschedulerschema-sendemailtype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                              | Derivato da                                                           | Descrizione                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**SendEmail (actionGroup)**](taskschedulerschema-sendemail-actiongroup-element.md) | [**sendEMailType**](taskschedulerschema-sendemailtype-complextype.md) | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                          | Tipo                                                                    | Descrizione                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**File**](taskschedulerschema-file-attachmentstype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Specifica il percorso di un file inviato come allegato in un messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Attachments di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)

Per lo sviluppo di script, [**vedere EmailAction.Attachments.**](emailaction-attachments.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





