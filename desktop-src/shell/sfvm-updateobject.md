---
description: Aggiorna un oggetto passando un puntatore a una matrice di due puntatori agli elenchi di identificatori di elemento (PID). Usato da SHShellFolderView \_ Message.
title: SFVM_UPDATEOBJECT messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452845"
---
# <a name="sfvm_updateobject-message"></a>Messaggio SFVM \_ UPDATEOBJECT

Aggiorna un oggetto passando un puntatore a una matrice di due puntatori agli elenchi di identificatori di elemento (PID). Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppidl* \[ Pollici\]
</dt> <dd>

Indirizzo di una matrice di due PIDL. Il primo PIDL è il vecchio PIDL. Il secondo è una copia del file PIDL precedente con informazioni aggiornate. Il controllo sulla durata della copia appartiene alla visualizzazione dopo il completamento della chiamata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID listview dell'oggetto aggiornato se l'aggiornamento ha avuto esito positivo; In caso contrario, restituisce -1.

## <a name="remarks"></a>Commenti

Se l'aggiornamento ha avuto esito negativo, il chiamante deve liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




