---
description: "Consente all'oggetto callback di specificare un parametro di ordinamento predefinito. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETSORTDEFAULTS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980882"
---
# <a name="sfvm_getsortdefaults-message"></a>\_Messaggio SFVM GETSORTDEFAULTS

Consente all'oggetto callback di specificare un parametro di ordinamento predefinito. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iDirection* \[ out\]
</dt> <dd>

Direzione di ordinamento predefinita. Impostare questo parametro su un valore positivo per eseguire l'ordinamento in ordine crescente. Impostare questo parametro su zero o su un valore negativo per eseguire l'ordinamento in ordine decrescente.

</dd> <dt>

*IColumn* \[ out\]
</dt> <dd>

Colonna utilizzata per l'ordinamento. Questa operazione verrà passata a [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) nei 16 bit inferiori del relativo valore *lParam* .

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> : **SFVM \_ GETSORTDEFAULTS** non è riconosciuto dall'oggetto visualizzazione cartella di sistema.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
