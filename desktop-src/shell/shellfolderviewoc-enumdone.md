---
description: Indica che l'oggetto ShellFolderView ha terminato l'enumerazione del contenuto della cartella.
title: Evento ShellFolderViewOC. EnumDone (shldisp. h)
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
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994989"
---
# <a name="shellfolderviewocenumdone-event"></a>Evento ShellFolderViewOC. EnumDone

Indica che l'oggetto [**ShellFolderView**](shellfolderview.md) ha terminato l'enumerazione del contenuto della cartella.

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

L'oggetto [**ShellFolderView**](shellfolderview.md) deve enumerare il contenuto di una cartella prima di poterlo visualizzare. Con le cartelle di grandi dimensioni o che si trovano in un sistema remoto, questo processo può richiedere fino a diversi minuti. Durante questo periodo, viene visualizzata un'immagine di torcia elettrica animata che indica all'utente che l'elaborazione è in corso. Al termine dell'enumerazione, viene generato l'evento **EnumDone** e il grafico della torcia viene sostituito dal contenuto della cartella.

Fornire il codice di gestione degli eventi per questo evento, come illustrato di seguito.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




