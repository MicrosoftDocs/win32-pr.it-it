---
description: L'utente ha fatto clic su una espansione per espandere l'elemento specificato dalla struttura SMDATA di cui è stato fatto clic.
title: SMC_CHEVRONEXPAND messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 036c45c6bd0e156a17cbcf2f89d3f64b2f619d4b4a6eb7e0a19b70eb3295292c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968250"
---
# <a name="smc_chevronexpand-message"></a>Messaggio \_ CHEVRONEXPAND di SMC

L'utente ha fatto clic su una espansione per espandere l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) di cui è stato fatto clic.


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

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



 

 




