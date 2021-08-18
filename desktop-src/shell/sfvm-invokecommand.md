---
description: Notifica all'oggetto callback che uno dei relativi comandi di menu o barra degli strumenti è stato richiamato dall'utente. Usato da IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: SFVM_INVOKECOMMAND messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b33eba78e0680fe940569c7a7ccfb4a27c61c3ffcb6eead0f2ff6436ec74f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968650"
---
# <a name="sfvm_invokecommand-message"></a>Messaggio \_ INVOKECOMMAND SFVM

Notifica all'oggetto callback che uno dei relativi comandi di menu o barra degli strumenti è stato richiamato dall'utente. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd* \[ in\]
</dt> <dd>

ID di comando della barra degli strumenti o della voce di menu selezionata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio svolge essenzialmente la stessa funzione di un messaggio [**WM \_ COMMAND**](../menurc/wm-command.md) in una routine di finestra convenzionale. Consente all'oggetto callback di gestire tutti gli elementi aggiunti alla barra dei menu o Windows Explorer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
