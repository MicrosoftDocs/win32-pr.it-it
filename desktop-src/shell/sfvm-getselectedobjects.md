---
description: Recupera una matrice di puntatori a elenchi di identificatori di elemento (PIDL) per tutti gli oggetti selezionati. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_GETSELECTEDOBJECTS (Shlobj. h)
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
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885341"
---
# <a name="sfvm_getselectedobjects-message"></a>\_Messaggio SFVM GETSELECTEDOBJECTS

Recupera una matrice di puntatori a elenchi di identificatori di elemento (PIDL) per tutti gli oggetti selezionati. Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppidl* \[ out\]
</dt> <dd>Indirizzo di una matrice di PIDL di oggetti attualmente selezionati.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi nella matrice.

## <a name="remarks"></a>Commenti

Al termine, è necessario chiamare [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) su ogni membro della matrice per liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




