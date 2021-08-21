---
description: Notifica di salvare l'oggetto passato.
title: SMC_SETSFOBJECT messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4ac46fd69d4d91870dcd288190baac275b37a5f093b87646c17d19e479bd710e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968010"
---
# <a name="smc_setsfobject-message"></a>Messaggio SMC \_ SETSFOBJECT

Notifica di salvare l'oggetto passato.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Iid* 
</dt> <dd>

IID associato all'oggetto .

</dd> <dt>

*Pv* 
</dt> <dd>

Puntatore all'interfaccia sull'oggetto specificato da *iid*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

La **notifica SMC \_ SETSFOBJECT** viene usata con il flusso IID. \_ L'oggetto viene salvato in un formato persistente nel Registro di sistema e non viene eseguito alcun conteggio dei riferimenti sull'oggetto passato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




