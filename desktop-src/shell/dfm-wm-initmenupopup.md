---
description: Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.
title: Messaggio DFM_WM_INITMENUPOPUP (Shlobj. h)
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
ms.openlocfilehash: 1c89731bdffc0e7d902e6c83b9a4f208134b7cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128451"
---
# <a name="dfm_wm_initmenupopup-message"></a>DFM \_ WM \_ INITMENUPOPUP messaggio

Inviato quando un menu a discesa o un sottomenu sta per diventare attivo. Questo consente a un'applicazione di modificare il menu prima che venga visualizzato, senza modificare l'intero menu.


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Handle per il menu a discesa o il sottomenu.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

La parola di ordine inferiore specifica la posizione relativa in base zero della voce di menu che apre il menu a discesa o il sottomenu.

La parola più ordinata indica se il menu a discesa è il menu finestra. Se il menu è il menu finestra, questo parametro è **true**; in caso contrario, è **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




