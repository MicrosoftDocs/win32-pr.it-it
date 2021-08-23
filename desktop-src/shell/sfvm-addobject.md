---
description: Aggiunge un oggetto alla visualizzazione Shell. Usato dal messaggio \_ SHShellFolderView.
title: SFVM_ADDOBJECT messaggio (Shlobj.h)
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
ms.openlocfilehash: 441ddac74e1640b2f836686c171d6fc896cbccee2dd6325c31041903ba610b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661061"
---
# <a name="sfvm_addobject-message"></a>Messaggio SFVM \_ ADDOBJECT

Aggiunge un oggetto alla visualizzazione Shell. Usato da [**SHShellFolderView \_ Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pidl* \[ Pollici\]
</dt> <dd>Puntatore all'oggetto di interesse da aggiungere.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il nuovo ID dell'elemento listview dell'oggetto aggiunto se il processo ha avuto esito positivo; In caso contrario, restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




