---
description: SFVM \_ GETDETAILSOF può essere modificato o non disponibile.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6fd850a3f500a1d259ebdcae9e5c549ef76a8eab0d5e1d14c1385fbba8d27ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048450"
---
# <a name="sfvm_getdetailsof-message"></a>Messaggio SFVM \_ GETDETAILSOF

\[**SFVM \_ GETDETAILSOF** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

Consente all'oggetto callback di fornire i dettagli per un elemento in una cartella Shell. Usare solo se una chiamata a [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) ha esito negativo e non è disponibile alcun metodo [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) da chiamare. Usato da [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iColumn* \[ Pollici\]
</dt> <dd>

ID in base zero della colonna.

</dd> <dt>

*pDi* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) compilata con le informazioni richieste.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP con SP2<br/>                                                      |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
