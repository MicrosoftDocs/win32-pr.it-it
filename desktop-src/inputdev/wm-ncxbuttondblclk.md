---
title: Messaggio WM_NCXBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- Input della tastiera e del mouse WM_NCXBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302392"
---
# <a name="wm_ncxbuttondblclk-message"></a>\_Messaggio NCXBUTTONDBLCLK WM

Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area non client di una finestra. Questo messaggio viene inserito nella finestra che contiene il cursore. Se una finestra ha acquisito il mouse, questo messaggio non viene inviato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica il valore di hit test restituito dalla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dall'elaborazione del messaggio [**WM \_ NCHITTEST**](wm-nchittest.md) . Per un elenco dei valori di hit test, vedere **WM \_ NCHITTEST**.

La parola più ordinata indica il pulsante su cui è stato fatto doppio clic. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt></dt> <dt>0x0001</dt> XBUTTON1 </dl> | È stato fatto doppio clic sul primo pulsante X.<br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt></dt> <dt>0x0002</dt> XBUTTON2 </dl> | È stato fatto doppio clic sul secondo pulsante X.<br/> |



 

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

Una finestra non deve avere lo stile **cs \_ DBLCLKS** per ricevere i messaggi **WM \_ NCXBUTTONDBLCLK** . Il sistema genera un messaggio **WM \_ NCXBUTTONDBLCLK** quando l'utente preme, rilascia e preme di nuovo un pulsante X entro il limite di tempo doppio clic del sistema. Facendo doppio clic su uno di questi pulsanti vengono effettivamente generati quattro messaggi: [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md), **WM \_ NCXBUTTONDBLCLK** e **WM \_ NCXBUTTONUP** .

A differenza dei [**messaggi \_ WM NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)e [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata. In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

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

[**\_NCXBUTTONDOWN WM**](wm-ncxbuttondown.md)
</dt> <dt>

[**\_NCXBUTTONUP WM**](wm-ncxbuttonup.md)
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

 

