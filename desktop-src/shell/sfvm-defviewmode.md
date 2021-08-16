---
description: Consente all'oggetto callback di specificare la modalità di visualizzazione. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_DEFVIEWMODE messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 28958fd992f70924ebbd51c06090d3a55c0ef8e6418d1ee055c5eb534acb9d3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090161"
---
# <a name="sfvm_defviewmode-message"></a>Messaggio \_ SFVM DEFVIEWMODE

Consente all'oggetto callback di specificare la modalità di visualizzazione. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pViewMode* \[ Cambio\]
</dt> <dd>

Uno dei valori del [**tipo enumerato FOLDERVIEWMODE.**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
