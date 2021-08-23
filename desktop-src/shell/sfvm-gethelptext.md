---
description: Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_GETHELPTEXT messaggio (Shlobj.h)
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
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661021"
---
# <a name="sfvm_gethelptext-message"></a>Messaggio SFVM \_ GETHELPTEXT

Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_GETHELPTEXT 

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



 

 
