---
title: Elemento ClassID (comHandlerType)
description: Specifica l'identificatore della classe del gestore.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- Elemento ClassID Utilità di pianificazione
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479240"
---
# <a name="classid-comhandlertype-element"></a>Elemento ClassID (comHandlerType)

Specifica l'identificatore della classe del gestore.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

L'elemento **ClassID** è definito dal tipo complesso [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                             | Descrizione                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comgestore**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Specifica un'azione che attiva un gestore.<br/> |



## <a name="remarks"></a>Commenti

Le applicazioni definiscono l'identificatore di classe usando la proprietà [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) dell'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





