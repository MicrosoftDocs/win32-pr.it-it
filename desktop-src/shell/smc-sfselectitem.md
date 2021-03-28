---
description: L'utente ha selezionato l'elemento specificato dalla struttura SMDATA associata.
title: Messaggio SMC_SFSELECTITEM (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979807"
---
# <a name="smc_sfselectitem-message"></a>\_Messaggio SFSELECTITEM di SMC

L'utente ha selezionato l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.


```C++
SMC_SFSELECTITEM
            
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



 

 




