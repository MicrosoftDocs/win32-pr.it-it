---
description: Aggiorna un oggetto passando un puntatore a una matrice di due puntatori a elenchi di identificatori di elemento (PIDL). Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_UPDATEOBJECT (Shlobj. h)
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
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234085"
---
# <a name="sfvm_updateobject-message"></a>\_Messaggio SFVM UPDATEOBJECT

Aggiorna un oggetto passando un puntatore a una matrice di due puntatori a elenchi di identificatori di elemento (PIDL). Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppidl* \[ in\]
</dt> <dd>

Indirizzo di una matrice di due PIDL. Il primo PIDL è il PIDL precedente. Il secondo è una copia del vecchio PIDL con le informazioni aggiornate. Il controllo della durata della copia appartiene alla visualizzazione dopo il completamento della chiamata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ID ListView dell'oggetto aggiornato se l'aggiornamento è stato eseguito correttamente. in caso contrario, restituisce-1.

## <a name="remarks"></a>Commenti

Se l'aggiornamento non è riuscito, il chiamante deve liberare la memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




