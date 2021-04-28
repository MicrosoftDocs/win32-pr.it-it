---
description: "DFM_WM_INITMENUPOPUP: inviato quando un menu a discesa o un sottomenu sta per diventare attivo. In questo modo un'applicazione può modificare il menu prima che venga visualizzato, senza modificare l'intero menu."
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
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096999"
---
# <a name="dfm_wm_initmenupopup-message"></a>Messaggio \_ INITMENUPOPUP di DFM WM \_

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
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




