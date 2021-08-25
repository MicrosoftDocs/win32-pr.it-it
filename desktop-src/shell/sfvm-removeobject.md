---
description: Rimuove un oggetto dalla visualizzazione della shell. Usato dal messaggio \_ SHShellFolderView.
title: SFVM_REMOVEOBJECT messaggio (Shlobj.h)
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
ms.openlocfilehash: d5bb53da276e28d7598961cc8f68a2464f414db9a3eac2ddab769102149bf370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941951"
---
# <a name="sfvm_removeobject-message"></a>Messaggio \_ SFVM REMOVEOBJECT

Rimuove un oggetto dalla visualizzazione della shell. Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Pollici\]
</dt> <dd>PIDL dell'oggetto da rimuovere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento rimosso se è stato trovato un elemento corrispondente al PIDL specificato; In caso contrario, restituisce -1.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




