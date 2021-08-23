---
description: Notifica all'oggetto callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartella. Usato da IShellFolderViewCB::MessageSFVCB.
title: SFVM_COLUMNCLICK messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592701"
---
# <a name="sfvm_columnclick-message"></a>Messaggio SFVM \_ COLUMNCLICK

Notifica all'oggetto callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartella. Usato da [**IShellFolderViewCB::MessageSFVCB.**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iColumn* \[ Pollici\]
</dt> <dd>

Indice della colonna su cui è stato fatto clic.

</dd> </dl>

## <a name="remarks"></a>Commenti

In risposta a questa notifica, è necessario restituire S \_ OK per ridisporre manualmente l'elenco. Per fare in modo che l'oggetto visualizzazione cartella di sistema riorganizza l'elenco, restituire S \_ FALSE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
