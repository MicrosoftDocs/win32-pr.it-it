---
title: Elemento title (showMessageType)
description: Contiene il titolo della finestra di messaggio.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Utilità di pianificazione elemento titolo
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119215"
---
# <a name="title-showmessagetype-element"></a>Elemento title (showMessageType)

Contiene il titolo della finestra di messaggio.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

L'elemento **title** è definito dal tipo complesso [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                               | Descrizione                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Rappresenta un'azione che visualizza una finestra di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**proprietà title di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Per lo sviluppo di script, vedere [**ShowMessageAction. title**](showmessageaction-title.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





