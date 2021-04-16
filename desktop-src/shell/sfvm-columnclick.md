---
description: "Notifica all'oggetto di callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartelle. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_COLUMNCLICK (Shlobj. h)
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
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485516"
---
# <a name="sfvm_columnclick-message"></a>\_Messaggio SFVM COLUMNCLICK

Notifica all'oggetto di callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartelle. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IColumn* \[ in\]
</dt> <dd>

Indice della colonna su cui è stato fatto clic.

</dd> </dl>

## <a name="remarks"></a>Commenti

In risposta a questa notifica, è necessario restituire S \_ OK per ridisporre l'elenco. Per fare in modo che l'oggetto visualizzazione cartella di sistema ridisponga l'elenco, restituire S \_ false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
