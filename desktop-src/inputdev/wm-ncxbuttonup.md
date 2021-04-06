---
title: Messaggio WM_NCXBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- Input della tastiera e del mouse WM_NCXBUTTONUP messaggio
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
ms.openlocfilehash: 6330849a433787dd09fad536f005d91f60376013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742346"
---
# <a name="wm_ncxbuttonup-message"></a>\_Messaggio NCXBUTTONUP WM

Inviato quando l'utente rilascia il primo o il secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio *non* viene inviato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dall'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) . Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.

La parola più ordinata indica quale pulsante è stato rilasciato. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt></dt> <dt>0x0001</dt> XBUTTON1 </dl> | Il primo pulsante X è stato rilasciato.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt></dt> <dt>0x0002</dt> XBUTTON2 </dl> | Il secondo pulsante X è stato rilasciato.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) che contiene le coordinate x e y del cursore. Le coordinate sono relative all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**. Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel parametro *wParam* .


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
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testa il punto specificato per ottenere la posizione del cursore ed esegue l'azione appropriata. Se appropriato, invia il messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra.

A differenza dei [**messaggi \_ WM NCLBUTTONUP**](wm-nclbuttonup.md), [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)e [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata. In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**\_NCHITTEST WM**](wm-nchittest.md)
</dt> <dt>

[**\_NCXBUTTONDBLCLK WM**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**\_NCXBUTTONDOWN WM**](wm-ncxbuttondown.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTI**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

