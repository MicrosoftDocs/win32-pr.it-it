---
description: Fornisce informazioni sull'operazione di sospensione di un'app.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaccia ISuspendingOperation (Windows. ApplicationModel.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: f17cd3d3b1eab67d0abfea200e657d8c4a17d8df9e3bb850e4ea361a760d19df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758631"
---
# <a name="isuspendingoperation-interface"></a>Interfaccia ISuspendingOperation

Fornisce informazioni sull'operazione di sospensione di un'app.

## <a name="members"></a>Membri

**L'interfaccia ISuspendingOperation** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ISuspendingOperation.**



| Metodo                                                  | Descrizione                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Richiede che l'operazione di sospensione dell'app sia posticipata.<br/> |



 

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **ISuspendingOperation.**



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Scadenza**](isuspendingoperation-deadline.md)<br/> | Lettura/Scrittura<br/> | Ottiene il tempo rimanente prima che un'operazione di sospensione dell'app ritardata continui.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
