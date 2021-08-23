---
title: WM_NCXBUTTONDOWN messaggio (Winuser.h)
description: Pubblicato quando l'utente preme il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene pubblicato.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- WM_NCXBUTTONDOWN messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17097748b064fe125bac20240f14684dfe01b560485c926e36e868da223e7d7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666261"
---
# <a name="wm_ncxbuttondown-message"></a>Messaggio \_ WM NCXBUTTONDOWN

Pubblicato quando l'utente preme il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio *non viene* pubblicato.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine basso specifica il valore dell'hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dall'elaborazione del [**messaggio WM \_ NCHITTEST.**](wm-nchittest.md) Per un elenco di valori di hit test, vedere **WM \_ NCHITTEST**. La parola più alta indica quale pulsante è stato premuto. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | È stato premuto il primo pulsante X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | È stato premuto il secondo pulsante X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.** Per altre informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel *parametro wParam.*


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



È anche possibile usare il codice seguente per ottenere le coordinate x e y da *lParam*:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per ottenere la posizione del cursore ed esegue l'azione appropriata. Se appropriato, invia il [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

A differenza dei messaggi [**WM \_ NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)e [**WM \_ NCRBUTTONDOWN,**](wm-ncrbuttondown.md) un'applicazione deve restituire **TRUE** da questo messaggio se lo elabora. In questo modo il software che simula questo messaggio nei sistemi Windows precedenti Windows 2000 sarà in grado di determinare se la routine della finestra ha elaborato il messaggio o ha chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINT**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

