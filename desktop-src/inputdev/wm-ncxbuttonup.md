---
title: WM_NCXBUTTONUP messaggio (Winuser.h)
description: Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio non viene inviato.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- WM_NCXBUTTONUP messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eab2067d3d16c3ae0864ba7ddf04b5666efa0186d0a7d55ebd5eddaa7533790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829901"
---
# <a name="wm_ncxbuttonup-message"></a>Messaggio \_ WM NCXBUTTONUP

Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inviato alla finestra che contiene il cursore. Se il mouse è stato acquisito da una finestra, questo messaggio *non viene* inviato.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa specifica il valore dell'hit test restituito dalla funzione [**DefWindowProc dall'elaborazione**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) del [**messaggio WM \_ NCHITTEST.**](wm-nchittest.md) Per un elenco di valori di hit test, vedere **WM \_ NCHITTEST.**

La parola più alta indica quale pulsante è stato rilasciato. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | È stato rilasciato il primo pulsante X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | Il secondo pulsante X è stato rilasciato.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura POINTS**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

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

 

Per impostazione predefinita, [**la funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verifica il punto specificato per ottenere la posizione del cursore ed esegue l'azione appropriata. Se appropriato, invia il [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra.

A differenza dei messaggi [**\_ WM NCLBUTTONUP**](wm-nclbuttonup.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)e [**WM \_ NCRBUTTONUP,**](wm-ncrbuttonup.md) un'applicazione deve restituire **TRUE** da questo messaggio se viene elaborata. In questo modo il software che simula questo messaggio in sistemi Windows precedenti Windows 2000 può determinare se la procedura finestra ha elaborato il messaggio o ha chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

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

[**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PUNTI DI APPLICAZIONE**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

