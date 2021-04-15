---
title: Elemento Body (showMessageType)
description: Contiene il testo da visualizzare nel corpo della finestra di messaggio.
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
keywords:
- Utilità di pianificazione elemento Body
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477470"
---
# <a name="body-showmessagetype-element"></a>Elemento Body (showMessageType)

Contiene il testo da visualizzare nel corpo della finestra di messaggio.

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

L'elemento **Body** è definito dal tipo complesso [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                               | Descrizione                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [**ShowMessage (actionGroup)**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Rappresenta un'azione che visualizza una finestra di messaggio.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà MessageBody di IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).

Per lo sviluppo di script, vedere [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





