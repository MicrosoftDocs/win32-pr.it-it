---
description: "Notifica all'oggetto callback che si è verificato un evento che interessa uno dei relativi elementi. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_FSNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2021
ms.locfileid: "104995221"
---
# <a name="sfvm_fsnotify-message"></a>\_Messaggio SFVM FSNOTIFY

Notifica all'oggetto callback che si è verificato un evento che interessa uno dei relativi elementi. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppidl* \[ in\]
</dt> <dd>

Puntatore di PIDL dell'elemento interessato.

</dd> <dt>

*Levent* \[ in\]
</dt> <dd>

Valore SHCNE che indica l'evento che si è verificato. Per un elenco di valori possibili, vedere [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
