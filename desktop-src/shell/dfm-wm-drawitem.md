---
description: Inviato alla finestra padre di un controllo o di un menu creato dal proprietario quando un aspetto visivo del controllo o del menu è stato modificato.
ms.assetid: 2515bbab-025f-4f00-8564-a732d68edea3
title: Messaggio DFM_WM_DRAWITEM (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67255fea5c39bebc995e5c53d90378536b12921b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977266"
---
# <a name="dfm_wm_drawitem-message"></a>\_Messaggio DFM WM \_ DrawItem

Inviato alla finestra padre di un controllo o di un menu creato dal proprietario quando un aspetto visivo del controllo o del menu è stato modificato.


```C++
DFM_WM_DRAWITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPDRAWITEMSTRUCT) lpDrawItem;

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Identificatore del controllo che ha inviato il messaggio **DFM \_ WM \_ DrawItem** . Se il messaggio è stato inviato da un menu, questo parametro è zero.

</dd> <dt>

*lpDrawItem* \[ out\]
</dt> <dd>

Puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente le informazioni sull'elemento da disegnare e il tipo di disegno necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**.

## <a name="remarks"></a>Commenti

Il membro **itemAction** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.

Prima di restituire l'elaborazione di questo messaggio, un'applicazione deve garantire che il contesto di dispositivo identificato dal membro **HDC** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
