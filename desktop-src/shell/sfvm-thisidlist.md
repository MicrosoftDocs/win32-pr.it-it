---
description: SFVM \_ THISIDLIST può essere modificato o non disponibile.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Messaggio SFVM_THISIDLIST (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760196"
---
# <a name="sfvm_thisidlist-message"></a>\_Messaggio SFVM THISIDLIST

\[**SFVM \_ THISIDLIST** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di specificare il puntatore della visualizzazione a un elenco di identificatori di elemento (PIDL). Viene usato solo quando [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) e [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) hanno avuto esito negativo. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PIDL* \[ out\]
</dt> <dd>

Indirizzo della PIDL della visualizzazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
