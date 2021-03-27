---
description: Richiede il titolo e il testo per un infotip della freccia di espansione per l'elemento specificato dalla struttura SMDATA associata.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Messaggio SMC_CHEVRONGETTIP (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980175"
---
# <a name="smc_chevrongettip-message"></a>\_Messaggio CHEVRONGETTIP di SMC

Richiede il titolo e il testo per un infotip della freccia di espansione per l'elemento specificato dalla struttura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associata.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che contiene il titolo di infotip. Questa stringa non deve essere più lunga di un massimo di \_ caratteri di percorso, incluso il carattere di terminazione **null** .

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Puntatore a un buffer che riceve una stringa Unicode con terminazione **null** che contiene il testo del infotip. Questa stringa non deve essere più lunga di un massimo di \_ caratteri di percorso, incluso il carattere di terminazione **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questa notifica viene ricevuta dal metodo [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




