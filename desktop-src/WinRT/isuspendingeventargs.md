---
description: Fornisce i dati per un evento di sospensione dell'app.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interfaccia ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307070"
---
# <a name="isuspendingeventargs-interface"></a>Interfaccia ISuspendingEventArgs

Fornisce i dati per un evento di sospensione dell'app.

## <a name="members"></a>Membri

L'interfaccia **ISuspendingEventArgs** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingEventArgs** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **ISuspendingEventArgs** ha queste proprietà.



| Proprietà                                                                           | Tipo di accesso           | Descrizione                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Lettura/Scrittura<br/> | Ottiene l'operazione di sospensione dell'app.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile accedere a questo oggetto quando si implementano i gestori eventi come [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)e si [**aggiunge la \_ sospensione**](/previous-versions//hh438376(v=vs.85)) per rispondere agli eventi di sospensione dell'app.

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

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
