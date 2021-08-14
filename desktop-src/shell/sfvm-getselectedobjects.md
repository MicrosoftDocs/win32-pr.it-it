---
description: Recupera una matrice di puntatori agli elenchi di identificatori di elemento (PID) per tutti gli oggetti selezionati. Usato da SHShellFolderView \_ Message.
title: SFVM_GETSELECTEDOBJECTS messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7e892755b3c9bec0d955ddc786b818eac8d04e865acb710d1d5064c7f4102e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677224"
---
# <a name="sfvm_getselectedobjects-message"></a>Messaggio SFVM \_ GETSELECTEDOBJECTS

Recupera una matrice di puntatori agli elenchi di identificatori di elemento (PID) per tutti gli oggetti selezionati. Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppidl* \[ Cambio\]
</dt> <dd>Indirizzo di una matrice di PIDL degli oggetti attualmente selezionati.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi nella matrice.

## <a name="remarks"></a>Commenti

Al termine, è necessario chiamare [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) su ogni membro della matrice per liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




