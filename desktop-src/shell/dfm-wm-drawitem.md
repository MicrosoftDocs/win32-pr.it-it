---
description: Inviato alla finestra padre di un controllo o di un menu disegnato dal proprietario quando viene modificato un aspetto visivo del controllo o del menu.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: DFM_WM_DRAWITEM messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7190d445490b581967c8dda67e170eb5db5665dfa59302313d7af736b275944d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969470"
---
# <a name="dfm_wm_drawitem-message"></a>Messaggio WM \_ DRAWITEM DFM \_

Inviato alla finestra padre di un controllo o di un menu disegnato dal proprietario quando viene modificato un aspetto visivo del controllo o del menu.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Identificatore del controllo che ha inviato il messaggio **\_ WM \_ DRAWITEM di DFM.** Se il messaggio è stato inviato da un menu, questo parametro è zero.

</dd> <dt>

*lpDrawItem* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente informazioni sull'elemento da disegnare e sul tipo di disegno richiesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.**

## <a name="remarks"></a>Commenti

Il **membro itemAction** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.

Prima di tornare dall'elaborazione di questo messaggio, un'applicazione deve garantire che il contesto di dispositivo identificato dal membro **hDC** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
