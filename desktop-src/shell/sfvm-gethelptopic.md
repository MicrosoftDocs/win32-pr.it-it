---
description: "Consente all'oggetto callback di specificare un file della Guida HTML e un argomento al suo interno. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETHELPTOPIC (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883422"
---
# <a name="sfvm_gethelptopic-message"></a>\_Messaggio SFVM GETHELPTOPIC

Consente all'oggetto callback di specificare un file della Guida HTML e un argomento al suo interno. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PhtD* \[ out\]
</dt> <dd>

Indirizzo di una struttura [**di \_ \_ dati SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) che specifica il file della Guida HTML e l'argomento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
