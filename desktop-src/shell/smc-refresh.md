---
description: Invia una notifica che indica che i menu sono stati completamente aggiornati ed è possibile reimpostare lo stato.
title: SMC_REFRESH messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 31ac0164ed3cd69dbeb71adc44c6e3a15b9092db79c7972800068dc06a378786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047002"
---
# <a name="smc_refresh-message"></a>Messaggio REFRESH di \_ SMC

Invia una notifica che indica che i menu sono stati completamente aggiornati ed è possibile reimpostare lo stato.


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




