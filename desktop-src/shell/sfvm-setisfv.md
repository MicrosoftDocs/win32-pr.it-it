---
description: Notifica all'oggetto callback del sito contenitore. Viene usato solo quando IObjectWithSite::SetSite non è supportato e viene usato SHCreateShellFolderViewEx. Usato da IShellFolderViewCB::MessageSFVCB.
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: SFVM_SETISFV messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660801"
---
# <a name="sfvm_setisfv-message"></a>Messaggio \_ SFVM SETISFV

\[Questa notifica è supportata tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003. Potrebbe non essere supportato nelle versioni successive di Windows.\]

Notifica all'oggetto callback del sito contenitore. Viene usato solo quando [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) non è supportato e [**viene usato SHCreateShellFolderViewEx.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sito* \[ Pollici\]
</dt> <dd>

Puntatore all'interfaccia [**IUnknown del sito contenitore.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
