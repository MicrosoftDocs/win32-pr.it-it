---
description: Associa una nuova icona grande o piccola a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.
ms.assetid: c86620f2-893b-46f8-8254-1d7c4c142f37
title: Messaggio WM_SETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bec7fc653123ba0a950c96bc1f54ebf436b0d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231544"
---
# <a name="wm_seticon-message"></a>\_Messaggio dell'icona WM

Associa una nuova icona grande o piccola a una finestra. Il sistema Visualizza l'icona grande nella finestra di dialogo ALT + TAB e l'icona piccola nella didascalia della finestra.


```C++
#define WM_SETICON                      0x0080
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di icona da impostare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                       | Significato                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Icona \_ di BIG**</dt> <dt>1</dt> </dl>       | Impostare l'icona grande per la finestra.<br/> |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Icona \_ di PICCOLO**</dt> <dt>0</dt> </dl> | Impostare l'icona piccola per la finestra.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la nuova icona grande o piccola. Se questo parametro è **null**, l'icona indicata da *wParam* viene rimossa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è un handle per l'icona grande o piccola precedente, a seconda del valore di *wParam*. È **null** se la finestra in precedenza non aveva alcuna icona del tipo indicato da *wParam*.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce un handle per l'icona grande o piccola precedente associata alla finestra, a seconda del valore di *wParam*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_icona WM GETicon**](wm-geticon.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
