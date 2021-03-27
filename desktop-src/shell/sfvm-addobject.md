---
description: Aggiunge un oggetto alla visualizzazione Shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_ADDOBJECT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994888"
---
# <a name="sfvm_addobject-message"></a>\_Messaggio SFVM AddObject

Aggiunge un oggetto alla visualizzazione Shell. Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PIDL* \[ in\]
</dt> <dd>Puntatore all'oggetto di interesse da aggiungere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il nuovo ID dell'elemento ListView dell'oggetto aggiunto se il processo ha avuto esito positivo; in caso contrario, restituisce-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




