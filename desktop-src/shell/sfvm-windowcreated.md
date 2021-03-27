---
description: "Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_WINDOWCREATED (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980866"
---
# <a name="sfvm_windowcreated-message"></a>\_Messaggio SFVM WINDOWCREATED

Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndView* \[ in\]
</dt> <dd>

Handle della finestra della visualizzazione cartelle.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
