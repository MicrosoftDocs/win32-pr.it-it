---
description: Imposta la posizione di un elemento nella visualizzazione della shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETITEMPOS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233886"
---
# <a name="sfvm_setitempos-message"></a>\_Messaggio SFVM SETITEMPOS

Imposta la posizione di un elemento nella visualizzazione della shell. Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SIP* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ SETITEMPOS SFV**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




