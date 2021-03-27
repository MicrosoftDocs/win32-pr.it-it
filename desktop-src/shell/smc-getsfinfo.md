---
description: Richiede informazioni su una voce di menu della cartella della shell.
title: Messaggio SMC_GETSFINFO (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994837"
---
# <a name="smc_getsfinfo-message"></a>\_Messaggio GETSFINFO di SMC

Richiede informazioni su una voce di menu della cartella della shell.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*psminfo* 
</dt> <dd>

Puntatore a una struttura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) . Compilare la struttura con le informazioni appropriate e restituire S \_ OK.

</dd> </dl>

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



 

 




