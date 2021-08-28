---
description: Consente all'oggetto callback di unire le voci di menu nei menu Windows Explorer. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_MERGEMENU messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5f6838b3c2ee845794bfa506beada2b7092f1bb918438f820f0e77d6b6543dc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111171"
---
# <a name="sfvm_mergemenu-message"></a>Messaggio \_ MERGEMENU SFVM

Consente all'oggetto callback di unire le voci di menu nei menu Windows Explorer. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ Cambio\]
</dt> <dd>

Struttura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni necessarie per unire le voci nel menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio ha essenzialmente lo stesso scopo di [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in una visualizzazione cartella personalizzata. Per altre informazioni, vedere la sezione Using *IShellBrowser to Communicate with Windows Explorer* (Uso di IShellBrowser per comunicare con Windows Explorer) di [Implementing a Folder View](../lwef/nse-folderview.md) (Implementazione di una visualizzazione cartelle).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
