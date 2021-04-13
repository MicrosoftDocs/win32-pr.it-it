---
title: Elemento file (attachmentsType)
description: Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Utilità di pianificazione elemento file
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400476"
---
# <a name="file-attachmentstype-element"></a>Elemento file (attachmentsType)

Contiene il percorso di un file inviato come allegato in un messaggio di posta elettronica.

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

L'elemento **file** è definito dal tipo complesso [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                      | Derivato da                                                               | Descrizione                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Allegati (sendEmailType)**](taskschedulerschema-attachments-sendemailtype-element.md) | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) | Contiene un elenco di allegati nel messaggio di posta elettronica.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà Attachments di IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).

Per lo sviluppo di script, vedere [**EmailAction. Attachments**](emailaction-attachments.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





