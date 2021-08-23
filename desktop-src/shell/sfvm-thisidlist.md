---
description: SFVM \_ THISIDLIST può essere modificato o non disponibile.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: SFVM_THISIDLIST messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd00f1cfc2b6661dac2414f0327cab03d4c0586eb62b992b5e33f81e64565246
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968630"
---
# <a name="sfvm_thisidlist-message"></a>Messaggio DI SFVM \_ THISIDLIST

\[**SFVM \_ THISIDLIST** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di specificare il puntatore della visualizzazione a un elenco di identificatori di elemento (PIDL). Viene usato solo quando [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) e [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) hanno avuto esito negativo. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Cambio\]
</dt> <dd>

Indirizzo del PIDL della vista.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
