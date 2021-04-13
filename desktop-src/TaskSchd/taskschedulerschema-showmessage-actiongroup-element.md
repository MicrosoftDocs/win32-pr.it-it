---
title: Elemento ShowMessage (actionGroup)
description: Rappresenta un'azione che visualizza una finestra di messaggio.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- Utilità di pianificazione elemento ShowMessage
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340493"
---
# <a name="showmessage-actiongroup-element"></a>Elemento ShowMessage (actionGroup)

Rappresenta un'azione che visualizza una finestra di messaggio.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

L'elemento **ShowMessage** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

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

Per lo sviluppo di script, viene specificata un'azione MessageBox utilizzando l'oggetto [**ShowMessageAction**](showmessageaction.md) .

Per lo sviluppo in C++, un'azione della finestra di messaggio viene specificata tramite l'interfaccia [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .

**Windows 8 e Windows Server 2012:** Questo elemento è stato rimosso. È possibile utilizzare IExecAction con la funzione Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) per visualizzare un messaggio nella sessione utente.

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un'azione MessageBox, vedere [esempio di finestra di messaggio (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |
| Fine del supporto client<br/>    | Windows 7<br/>                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                    |



 

