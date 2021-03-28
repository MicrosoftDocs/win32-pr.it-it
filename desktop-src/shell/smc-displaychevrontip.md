---
description: Notifica all'utente che sta per essere visualizzato un infotip per la freccia di espansione associata all'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_DISPLAYCHEVRONTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485508"
---
# <a name="smc_displaychevrontip-message"></a>\_Messaggio DISPLAYCHEVRONTIP di SMC

Notifica all'utente che sta per essere visualizzato un infotip per la freccia di espansione associata all'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

## <a name="return-value"></a>Valore restituito

Restituire S \_ OK per visualizzare il infotip. Restituisce \_ false per impedire la visualizzazione del infotip.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




