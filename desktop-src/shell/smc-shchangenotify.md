---
description: Notifica all'utente che è stata apportata una modifica.
title: SMC_SHCHANGENOTIFY messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8232f170-0dab-475a-ace0-67c04f01c777
api_name:
- SMC_SHCHANGENOTIFY
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9a74f0716eed49a964002e7f6bb1fa8b513fa968eff32d9ed67fa26a1364bcfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967960"
---
# <a name="smc_shchangenotify-message"></a>Messaggio \_ SHCHANGENOTIFY di SMC

Notifica all'utente che è stata apportata una modifica.


```C++
SMC_SHCHANGENOTIFY
    lParam = (LPARAM) (PSMCSCHANGENOTIFYSTRUCT) psmc
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psmc* 
</dt> <dd>

Puntatore a una [**struttura SMCSHCHANGENOTIFYSTRUCT**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct) con informazioni sulla modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire S \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




