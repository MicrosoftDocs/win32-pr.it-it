---
description: Indica che l'oggetto ShellFolderView ha terminato l'enumerazione del contenuto della cartella.
title: Evento ShellFolderViewOC.EnumDone (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: c725a61a6711dab22d50b774cb02556916dae802a66008a48721d7311e163bce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660641"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC.EnumDone

Indica che [**l'oggetto ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.

## <a name="syntax"></a>Sintassi


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Parametri

Questo gestore eventi non ha parametri.

## <a name="remarks"></a>Commenti

[**L'oggetto ShellFolderView**](shellfolderview.md) deve enumerare il contenuto di una cartella prima di poterla visualizzare. Con le cartelle di grandi dimensioni o che si trovano in un sistema remoto, questo processo può richiedere fino a diversi minuti. Durante questo periodo, viene visualizzata una torcia animata per indicare all'utente che è in corso l'elaborazione. Al termine dell'enumerazione, viene generato l'evento **EnumDone** e il grafico torcia viene sostituito dal contenuto della cartella.

Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




