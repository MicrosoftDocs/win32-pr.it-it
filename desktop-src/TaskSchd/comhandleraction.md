---
title: Oggetto ComHandlerAction
description: Oggetto di scripting che rappresenta un'azione che attiva un gestore.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Utilità di pianificazione azione gestore COM, oggetto
- Utilità di pianificazione oggetto ComHandlerAction
- Oggetto ComHandlerAction Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475046"
---
# <a name="comhandleraction-object"></a>Oggetto ComHandlerAction

Oggetto di scripting che rappresenta un'azione che attiva un gestore.

## <a name="members"></a>Membri

L'oggetto **ComHandlerAction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ComHandlerAction** dispone di queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassId**](comhandleraction-classid.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore della classe del gestore.<br/>                                              |
| [**Data**](comhandleraction-data.md)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta dati aggiuntivi associati al gestore.<br/>                              |
| [**ID**](action-id.md)<br/>                     | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**azione**](action.md) . Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Sola lettura<br/>  | Ereditato dall'oggetto [**azione**](action.md) . Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

I gestori COM devono implementare l'interfaccia [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) per l'utilità di pianificazione per avviare e arrestare il gestore. Il gestore COM utilizza a sua volta i metodi dell'oggetto [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) per comunicare lo stato al utilità di pianificazione.

Durante la lettura o la scrittura di codice XML, un'azione del gestore COM viene specificata nell'elemento [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





