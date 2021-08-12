---
title: Elemento ShowMessage (actionGroup)
description: Rappresenta un'azione che mostra una finestra di messaggio.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Elemento ShowMessage Utilità di pianificazione
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474bc44550408591616d3a8d2c6c3c69a5a0d073c90297c60b4a831627c996e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611299"
---
# <a name="showmessage-actiongroup-element"></a>Elemento ShowMessage (actionGroup)

Rappresenta un'azione che mostra una finestra di messaggio.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

**L'elemento ShowMessage** è definito dall'elemento [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                    | Derivato da                                                       | Descrizione                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Azioni (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene le azioni eseguite dall'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                            | Tipo           | Descrizione                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Corpo**](taskschedulerschema-body-showmessagetype-element.md)   | nonEmptyString | Specifica il testo da visualizzare nel corpo della finestra di messaggio. <br/> |
| [**Titolo**](taskschedulerschema-title-showmessagetype-element.md) | nonEmptyString | Specifica il titolo della finestra di messaggio. <br/>                       |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, viene specificata un'azione della finestra di messaggio usando [**l'oggetto ShowMessageAction.**](showmessageaction.md)

Per lo sviluppo C++, viene specificata un'azione della finestra di messaggio tramite [**l'interfaccia IShowMessageAction.**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)

**Windows 8 e Windows Server 2012:** Questo elemento è stato rimosso. È possibile usare IExecAction con la Windows [**msgBox**](/previous-versions/sfw6660x(v=vs.80)) di scripting per visualizzare un messaggio nella sessione utente.

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un'azione della finestra di messaggio, vedere Esempio di finestra di [messaggio (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |
| Fine del supporto client<br/>    | Windows 7<br/>                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                    |



 

