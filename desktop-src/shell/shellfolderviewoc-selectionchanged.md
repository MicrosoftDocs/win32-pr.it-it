---
description: Indica che lo stato di selezione di uno o più elementi nella visualizzazione è stato modificato.
title: Evento ShellFolderViewOC.SelectionChanged (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 264631c43dd9ac20bd0ae47632738c2a37a0a85168b487e17ff86a8a2b71c8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660631"
---
# <a name="shellfolderviewocselectionchanged-event"></a>Evento ShellFolderViewOC.SelectionChanged

Indica che lo stato di selezione di uno o più elementi nella visualizzazione è stato modificato.

## <a name="syntax"></a>Sintassi


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parametri

Questo gestore eventi non ha parametri.

## <a name="remarks"></a>Commenti

Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




