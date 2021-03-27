---
description: Rimuove un oggetto dalla visualizzazione Shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_REMOVEOBJECT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980887"
---
# <a name="sfvm_removeobject-message"></a>\_Messaggio SFVM RemoveObject

Rimuove un oggetto dalla visualizzazione Shell. Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PIDL* \[ in\]
</dt> <dd>PIDL dell'oggetto da rimuovere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento che è stato rimosso se è stato trovato un elemento corrispondente all'oggetto PIDL specificato. in caso contrario, restituisce-1.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




