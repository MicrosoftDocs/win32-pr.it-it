---
title: Elemento Body (showMessageType)
description: Contiene il testo da visualizzare nel corpo della finestra di messaggio.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Corpo dell'Utilità di pianificazione
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6b1fbacd450c05b8ff71521dacfa6e95c7efc70fc7d8909ca66f3390bf22295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010871"
---
# <a name="body-showmessagetype-element"></a>Elemento Body (showMessageType)

Contiene il testo da visualizzare nel corpo della finestra di messaggio.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

**L'elemento** Body è definito dal [**tipo complesso showMessageType.**](taskschedulerschema-showmessagetype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                               | Descrizione                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Rappresenta un'azione che mostra una finestra di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere [**Proprietà MessageBody di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Per lo sviluppo di script, [**vedere ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





