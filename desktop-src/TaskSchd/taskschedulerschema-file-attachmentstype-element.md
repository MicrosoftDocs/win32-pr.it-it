---
title: Elemento File (attachmentsType)
description: Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Elemento File Utilità di pianificazione
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 793b23bc6b9d75ac809c42063fa9c300542705b718cd22253f6f2d3a1a76caa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125851"
---
# <a name="file-attachmentstype-element"></a>Elemento File (attachmentsType)

Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

**L'elemento File** è definito dal [**tipo complesso attachmentsType.**](taskschedulerschema-attachmentstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                      | Derivato da                                                               | Descrizione                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Allegati (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contiene un elenco di allegati nel messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Attachments di IEmailAction.**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)

Per lo sviluppo di script, [**vedere EmailAction.Attachments.**](emailaction-attachments.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





