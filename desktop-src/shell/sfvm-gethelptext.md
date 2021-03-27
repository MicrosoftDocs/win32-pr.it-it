---
description: "Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETHELPTEXT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757841"
---
# <a name="sfvm_gethelptext-message"></a>\_Messaggio SFVM GETHELPTEXT

Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

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



 

 
