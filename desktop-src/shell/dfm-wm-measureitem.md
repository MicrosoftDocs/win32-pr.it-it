---
description: Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: DFM_WM_MEASUREITEM messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ad0d39a56f598a8ef4773c70f4f438388e91a2154b3083fdf85a1ebebec22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860899"
---
# <a name="dfm_wm_measureitem-message"></a>Messaggio \_ MEASUREITEM WM DFM \_

Inviato alla finestra proprietaria di un controllo o di una voce di menu quando viene creato il controllo o il menu.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore del membro **CtlID** della struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta il *parametro lpMeasureItem.* Questo valore identifica il controllo che ha inviato il **messaggio \_ \_ MEASUREITEM WM DFM.**

</dd> <dt>

*lpMeasureItem* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) che contiene le dimensioni del controllo o della voce di menu disegnata dal proprietario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando la finestra proprietaria riceve il messaggio **\_ DFM WM \_ MEASUREITEM,** il proprietario inserisce la struttura [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) a cui punta *il parametro lpMeasureItem* del messaggio e restituisce un messaggio che informa il sistema delle dimensioni del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
