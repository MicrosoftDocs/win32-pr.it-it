---
description: Fornisce informazioni su un'operazione di sospensione dell'app.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaccia ISuspendingOperation (Windows. ApplicationModel. h)
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
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526221"
---
# <a name="isuspendingoperation-interface"></a>Interfaccia ISuspendingOperation

Fornisce informazioni su un'operazione di sospensione dell'app.

## <a name="members"></a>Membri

L'interfaccia **ISuspendingOperation** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **ISuspendingOperation** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Richiede che l'operazione di sospensione dell'app venga posticipata.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **ISuspendingOperation** ha queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Scadenza**](isuspendingoperation-deadline.md)<br/> | Lettura/Scrittura<br/> | Ottiene il tempo rimanente prima che un'operazione di sospensione dell'app ritardata continui.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
