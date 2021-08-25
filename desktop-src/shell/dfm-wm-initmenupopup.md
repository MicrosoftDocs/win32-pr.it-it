---
description: "DFM_WM_INITMENUPOPUP messaggio: inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu."
title: DFM_WM_INITMENUPOPUP messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4cb68b8251fa383ae9386eae3e6753158330c4be7566f02a8758a72dfe05de03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943151"
---
# <a name="dfm_wm_initmenupopup-message"></a>Messaggio DFM \_ WM \_ INITMENUPOPUP

Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Handle per il menu a discesa o il sottomenu.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

La parola meno ordinata specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.

La parola più importante indica se il menu a discesa è il menu della finestra. Se il menu è il menu della finestra, questo parametro è **TRUE**; in caso contrario, è **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




