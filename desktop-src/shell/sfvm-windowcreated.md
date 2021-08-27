---
description: Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_WINDOWCREATED messaggio (Shlobj.h)
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
ms.openlocfilehash: 2d09957e1164d5caacbddc23c9a72cb33ef80ffa156dd0538c0be1e24f192018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111161"
---
# <a name="sfvm_windowcreated-message"></a>MESSAGGIO \_ WINDOWCREATED SFVM

Notifica all'oggetto callback che è in corso la creazione della finestra di visualizzazione cartelle. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndView* \[ Pollici\]
</dt> <dd>

Handle di finestra della visualizzazione cartella.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
