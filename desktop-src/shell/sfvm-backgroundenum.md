---
description: Consente all'oggetto callback di richiedere l'enumerazione in un thread in background. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_BACKGROUNDENUM messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592741"
---
# <a name="sfvm_backgroundenum-message"></a>Messaggio SFVM \_ BACKGROUNDENUM

Consente all'oggetto callback di richiedere l'enumerazione in un thread in background. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

## <a name="remarks"></a>Commenti

In risposta a questa notifica, restituire S \_ OK per abilitare l'enumerazione in background. Per impostazione predefinita, l'oggetto cartella di sistema visualizza l'animazione "torcia" mentre è in corso l'enumerazione . Per specificare un'animazione personalizzata, gestire [**SFVM \_ GETANIMATION**](sfvm-getanimation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
