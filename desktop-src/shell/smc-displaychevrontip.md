---
description: Notifica all'utente che sta per essere visualizzata una descrizione comandi per la casella di controllo associata all'elemento specificato dalla struttura SMDATA associata.
title: SMC_DISPLAYCHEVRONTIP messaggio (Shobjidl.h)
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
ms.openlocfilehash: f1107af5cd621bafbc1e463101cee2ea57236b9d29844d6183963134b50ce3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968170"
---
# <a name="smc_displaychevrontip-message"></a>Messaggio \_ DISPLAYCHEVRONTIP di SMC

Notifica all'utente che sta per essere visualizzata una descrizione comandi per la casella di controllo associata all'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituire S \_ OK per visualizzare la descrizione comandi. Restituisce S \_ FALSE per impedire la visualizzazione della descrizione comandi.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




