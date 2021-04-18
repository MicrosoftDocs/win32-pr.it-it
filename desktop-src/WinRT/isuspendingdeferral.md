---
description: Gestisce un'operazione di sospensione dell'app ritardata.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interfaccia ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307071"
---
# <a name="isuspendingdeferral-interface"></a>Interfaccia ISuspendingDeferral

Gestisce un'operazione di sospensione dell'app ritardata.

## <a name="members"></a>Membri

L'interfaccia **ISuspendingDeferral** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingDeferral** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISuspendingDeferral** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Operazione completata**](isuspendingdeferral-complete.md) | Notifica al sistema che l'app ha salvato i dati ed è pronta per essere sospesa.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
