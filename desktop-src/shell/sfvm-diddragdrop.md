---
description: SFVM \_ DIDDRAGDROP può essere modificato o non disponibile.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Messaggio SFVM_DIDDRAGDROP (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994917"
---
# <a name="sfvm_diddragdrop-message"></a>\_Messaggio SFVM DIDDRAGDROP

\[**SFVM \_ DIDDRAGDROP** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Notifica alla funzione di callback che è iniziata un'operazione di trascinamento della selezione. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwEffect* \[ in\]
</dt> <dd>

Identificatore dell'effetto di rilascio dall'enumerazione [**DropEffect**](../com/dropeffect-constants.md) . Questa operazione viene ottenuta chiamando [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).

</dd> <dt>

*pIdo* \[ in\]
</dt> <dd>

Puntatore all'istanza di [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
