---
description: "Consente all'oggetto callback di unire le voci di menu nei menu di Esplora risorse. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_MERGEMENU (Shlobj. h)
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
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980831"
---
# <a name="sfvm_mergemenu-message"></a>\_Messaggio SFVM MERGEMENU

Consente all'oggetto callback di unire le voci di menu nei menu di Esplora risorse. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInfo* \[ out\]
</dt> <dd>

Struttura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni necessarie per unire gli elementi nel menu.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio ha essenzialmente lo stesso scopo di [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in una visualizzazione cartella personalizzata. Per ulteriori informazioni, vedere la sezione *uso di IShellBrowser per comunicare con Esplora risorse* di [implementazione di una visualizzazione cartella](../lwef/nse-folderview.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
