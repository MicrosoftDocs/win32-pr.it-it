---
description: "Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Messaggio SFVM_GETTOOLTIPTEXT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968519"
---
# <a name="sfvm_gettooltiptext-message"></a>\_Messaggio SFVM GETTOOLTIPTEXT

Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd \_ cchMax* \[\]
</dt> <dd>

La parola di basso livello di questo parametro include l'ID del comando. La parola più ordinata include il numero di caratteri nel buffer di *pszText* .

</dd> <dt>

*pszText* \[ out\]
</dt> <dd>

Stringa con terminazione null contenente il testo della guida.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
