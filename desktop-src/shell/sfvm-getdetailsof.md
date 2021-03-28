---
description: SFVM \_ GETDETAILSOF può essere modificato o non disponibile.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Messaggio SFVM_GETDETAILSOF (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980218"
---
# <a name="sfvm_getdetailsof-message"></a>\_Messaggio SFVM GETDETAILSOF

\[**SFVM \_ GETDETAILSOF** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di fornire i dettagli per un elemento in una cartella della shell. Usare solo se una chiamata a [**IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) ha esito negativo e non è disponibile alcun metodo [**IShellDetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) per chiamare. Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IColumn* \[ in\]
</dt> <dd>

ID in base zero della colonna.

</dd> <dt>

*pDi* \[ out\]
</dt> <dd>

Puntatore a una struttura [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) riempita con le informazioni richieste.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
