---
description: Notifica all'utente di inizializzare la banda di menu.
title: Messaggio SMC_INITMENU (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ed7f7be1786192fb2be42f6d36cfb4bf222136fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232329"
---
# <a name="smc_initmenu-message"></a>\_Messaggio INITMENU di SMC

Notifica all'utente di inizializzare la banda di menu.


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




