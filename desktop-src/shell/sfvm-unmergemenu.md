---
description: "Notifica all'oggetto callback che è in corso la rimozione di un menu. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_UNMERGEMENU (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980815"
---
# <a name="sfvm_unmergemenu-message"></a>\_Messaggio SFVM UNMERGEMENU

Notifica all'oggetto callback che è in corso la rimozione di un menu. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hmenuCurrent* \[ in\]
</dt> <dd>

Handle del menu da rimuovere.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
