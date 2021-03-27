---
description: "Consente all'oggetto callback di fornire una pagina da aggiungere alla finestra delle proprietà delle proprietà dell'oggetto selezionato. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_ADDPROPERTYPAGES (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994885"
---
# <a name="sfvm_addpropertypages-message"></a>\_Messaggio SFVM ADDPROPERTYPAGES

Consente all'oggetto callback di fornire una pagina da aggiungere alla finestra **delle proprietà delle proprietà dell'** oggetto selezionato. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ out\]
</dt> <dd>

Indirizzo di una struttura [**di \_ \_ dati SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio funge essenzialmente dalla stessa funzione di [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Per ulteriori informazioni, vedere [creazione di gestori della finestra delle proprietà](propsheet-handlers.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
