---
description: Notifica a IShellView quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETCLIPBOARD (Shlobj. h)
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
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995157"
---
# <a name="sfvm_setclipboard-message"></a>SFVM \_ messaggi degli Appunti

Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quando uno dei relativi oggetti viene inserito negli Appunti come risultato di un comando di menu. Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwEffect* \[ in\]
</dt> <dd>

Use (WPARAM)-2 se l'elemento viene tagliato negli Appunti o (WPARAM)-3 Se l'elemento viene copiato negli Appunti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




