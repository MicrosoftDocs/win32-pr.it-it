---
description: Richiede se è accettabile eliminare un oggetto dati nell'elemento specificato dalla struttura SMDATA associata.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Messaggio SMC_SFDDRESTRICTED (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980146"
---
# <a name="smc_sfddrestricted-message"></a>\_Messaggio SFDDRESTRICTED di SMC

Richiede se è accettabile eliminare un oggetto dati nell'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDropTarget* 
</dt> <dd>

Indirizzo di un puntatore void che riceve un puntatore all'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Impostare questo valore su **null** se non si desidera accettare l'oggetto dati.

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



 

 
