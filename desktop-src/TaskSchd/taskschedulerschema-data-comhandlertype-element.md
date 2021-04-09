---
title: Elemento data (comHandlerType)
description: Specifica i dati aggiuntivi associati al gestore.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Utilità di pianificazione elemento dati
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964674"
---
# <a name="data-comhandlertype-element"></a>Elemento data (comHandlerType)

Specifica i dati aggiuntivi associati al gestore.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

L'elemento **dati** è definito dal tipo complesso [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                             | Descrizione                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comgestore**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Specifica un'azione che attiva un gestore.<br/> |



## <a name="remarks"></a>Commenti

Le applicazioni definiscono i dati del gestore usando la proprietà [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) dell'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





