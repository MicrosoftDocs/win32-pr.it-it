---
title: Gruppo actionGroup
description: Definisce il gruppo di azioni che un'attività può eseguire.
ms.assetid: a43ba021-4a40-4e2c-a57f-bd6ee17706ba
keywords:
- Gruppo actionGroup Utilità di pianificazione
- Gruppo di Utilità di pianificazione
topic_type:
- apiref
api_name:
- actionGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcfd37187373e8bebdcc6b2af22323fd5475a6893791158b83b16c278752e420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357179"
---
# <a name="actiongroup-group"></a>Gruppo actionGroup

Definisce il gruppo di azioni che un'attività può eseguire.

``` syntax
<xs:group name="actionGroup">
    <xs:choice>
        <xs:element name="Exec"
            type="execType"
         />
        <xs:element name="ComHandler"
            type="comHandlerType"
         />
        <xs:element name="SendEmail"
            type="sendEmailType"
         />
        <xs:element name="ShowMessage"
            type="showMessageType"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo                                                                       | Descrizione                                                             |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)   | Rappresenta un'azione che genera un gestore.<br/>                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | [**execType**](taskschedulerschema-exectype-complextype.md)               | Rappresenta un'azione che esegue un'operazione della riga di comando.<br/> |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)     | Rappresenta un'azione che invia un messaggio di posta elettronica.<br/>            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) | Rappresenta un'azione che mostra una finestra di messaggio.<br/>               |



## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML, gli elementi definiti da questo gruppo sono gli elementi figlio [**dell'elemento**](taskschedulerschema-actions-tasktype-element.md) Actions.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





