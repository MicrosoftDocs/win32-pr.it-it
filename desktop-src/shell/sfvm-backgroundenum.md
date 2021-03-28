---
description: "Consente all'oggetto callback di richiedere l'enumerazione in un thread in background. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_BACKGROUNDENUM (Shlobj. h)
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
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994920"
---
# <a name="sfvm_backgroundenum-message"></a>\_Messaggio SFVM BACKGROUNDENUM

Consente all'oggetto callback di richiedere l'enumerazione in un thread in background. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parametri

Questo messaggio non contiene parametri.

## <a name="remarks"></a>Commenti

In risposta a questa notifica, restituire S \_ OK per abilitare l'enumerazione in background. Per impostazione predefinita, l'oggetto cartella di sistema visualizzerà l'animazione "torcia" mentre è in corso l'enumerazione. Per specificare un'animazione personalizzata, gestire [**SFVM \_ getanimation**](sfvm-getanimation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
