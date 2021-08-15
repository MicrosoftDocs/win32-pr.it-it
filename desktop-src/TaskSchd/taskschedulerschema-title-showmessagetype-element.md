---
title: Elemento Title (showMessageType)
description: Contiene il titolo della finestra di messaggio.
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Elemento Title Utilità di pianificazione
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e5fe72b791a963e78d49ace14f7edec1210dc3bf23a5f7cee9550e6f6db53e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355678"
---
# <a name="title-showmessagetype-element"></a>Elemento Title (showMessageType)

Contiene il titolo della finestra di messaggio.

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

**L'elemento Title** è definito dal [**tipo complesso showMessageType.**](taskschedulerschema-showmessagetype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                               | Descrizione                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Rappresenta un'azione che mostra una finestra di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, [**vedere Proprietà Title di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).

Per lo sviluppo di script, [**vedere ShowMessageAction.Title**](showmessageaction-title.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





