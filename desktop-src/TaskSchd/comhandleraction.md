---
title: Oggetto ComHandlerAction
description: Oggetto di scripting che rappresenta un'azione che genera un gestore.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Azione del gestore COM Utilità di pianificazione , oggetto
- Oggetto ComHandlerAction Utilità di pianificazione
- Oggetto ComHandlerAction Utilità di pianificazione , descritto
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
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659681"
---
# <a name="comhandleraction-object"></a>Oggetto ComHandlerAction

Oggetto di scripting che rappresenta un'azione che genera un gestore.

## <a name="members"></a>Membri

**L'oggetto ComHandlerAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ComHandlerAction** ha queste proprietà.



| Proprietà                                               | Tipo di accesso           | Descrizione                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Classid**](comhandleraction-classid.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'identificatore della classe del gestore.<br/>                                              |
| [**Dati**](comhandleraction-data.md)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta dati aggiuntivi associati al gestore.<br/>                              |
| [**Id**](action-id.md)<br/>                     | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto**](action.md) Action. Ottiene o imposta l'identificatore dell'azione.<br/> |
| [**Tipo**](action-type.md)<br/>                 | Sola lettura<br/>  | Ereditato [**dall'oggetto**](action.md) Action. Ottiene il tipo dell'azione.<br/>               |



 

## <a name="remarks"></a>Commenti

I gestori COM devono implementare [**l'interfaccia ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) per Utilità di pianificazione avviare e arrestare il gestore. A sua volta, il gestore COM usa i metodi [**dell'oggetto TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) per comunicare lo stato al Utilità di pianificazione.

Quando si legge o si scrive codice XML, viene specificata un'azione del gestore COM nell'elemento [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) Utilità di pianificazione schema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Utilità di pianificazione oggetti](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





