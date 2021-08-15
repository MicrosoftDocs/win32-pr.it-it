---
description: Richiede il titolo e il testo per una descrizione comandi di suggerimento per la descrizione comandi per l'elemento specificato dalla struttura SMDATA.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: SMC_CHEVRONGETTIP messaggio (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968240"
---
# <a name="smc_chevrongettip-message"></a>Messaggio DI \_ CHEVRONGETTIP di SMC

Richiede il titolo e il testo per una descrizione comandi di suggerimento per la descrizione comandi per l'elemento specificato dalla struttura [**SMDATA.**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata)


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Puntatore a un buffer che riceve una stringa Unicode con terminazione **NULL** che contiene il titolo della descrizione comandi. La lunghezza di questa stringa non deve essere superiore a MAX \_ PATH, incluso il carattere **NULL di** terminazione.

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Puntatore a un buffer che riceve una stringa Unicode con terminazione **NULL** che contiene il testo della descrizione comandi. La lunghezza di questa stringa non deve essere superiore a MAX \_ PATH, incluso il carattere **NULL di** terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituire S \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal [**metodo IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




