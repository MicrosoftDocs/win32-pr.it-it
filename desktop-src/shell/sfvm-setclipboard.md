---
description: Notifica a IShellView quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu. Usato da SHShellFolderView \_ Message.
title: SFVM_SETCLIPBOARD messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99548be90c7f4fb9b840e4d4c6f816710c6e02cc1a888ce0c1c774f73c58f668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858213"
---
# <a name="sfvm_setclipboard-message"></a>Messaggio \_ SFVM SETCLIPBOARD

Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu. Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwEffect* \[ Pollici\]
</dt> <dd>

Usare (WPARAM)-2 se l'elemento viene tagliato negli Appunti o (WPARAM)-3 se l'elemento viene copiato negli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




