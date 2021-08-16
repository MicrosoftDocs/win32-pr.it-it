---
description: Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB::MessageSFVCB.
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: SFVM_GETTOOLTIPTEXT messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350d1f772cd78c97f7b57b47084c761808583dfe5396fafcdad336291a3a717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858223"
---
# <a name="sfvm_gettooltiptext-message"></a>MESSAGGIO \_ SFVM GETTOOLTIPTEXT

Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ cchMax* \[ in\]
</dt> <dd>

La parola più bassa di questo parametro contiene l'ID del comando. La parola più alta contiene il numero di caratteri nel buffer *pszText.*

</dd> <dt>

*pszText* \[ Cambio\]
</dt> <dd>

Stringa con terminazione Null contenente il testo della Guida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
