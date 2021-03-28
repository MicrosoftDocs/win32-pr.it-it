---
description: "Notifica all'oggetto callback del sito contenitore. Viene usato solo quando IObjectWithSite:: SESITE non è supportato e viene usato SHCreateShellFolderViewEx. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Messaggio SFVM_SETISFV (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980879"
---
# <a name="sfvm_setisfv-message"></a>\_Messaggio SFVM SETISFV

\[Questa notifica è supportata tramite Windows XP Service Pack 2 (SP2) e Windows Server 2003. Potrebbe non essere supportata nelle versioni successive di Windows.\]

Notifica all'oggetto callback del sito contenitore. Viene usato solo quando [**IObjectWithSite:: SESITE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) non è supportato e viene usato [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) . Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sito* \[ di in\]
</dt> <dd>

Puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sito contenitore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
