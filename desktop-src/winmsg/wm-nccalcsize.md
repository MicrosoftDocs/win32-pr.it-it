---
description: Inviato quando devono essere calcolate le dimensioni e la posizione dell'area client di una finestra. Elaborando questo messaggio, un'applicazione può controllare il contenuto dell'area client della finestra quando le dimensioni o la posizione della finestra cambiano.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: WM_NCCALCSIZE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a73b469a920bcba79cc19670a7b9536c1bac9e0b0ffcab7ddf5930b984dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200077"
---
# <a name="wm_nccalcsize-message"></a>Messaggio \_ WM NCCALCSIZE

Inviato quando devono essere calcolate le dimensioni e la posizione dell'area client di una finestra. Elaborando questo messaggio, un'applicazione può controllare il contenuto dell'area client della finestra quando le dimensioni o la posizione della finestra cambiano.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se *wParam* è **TRUE,** specifica che l'applicazione deve indicare quale parte dell'area client contiene informazioni valide. Il sistema copia le informazioni valide nell'area specificata all'interno della nuova area client.

Se *wParam* è **FALSE,** l'applicazione non deve indicare la parte valida dell'area client.

</dd> <dt>

*lParam* 
</dt> <dd>

Se *wParam* è **TRUE,** *lParam* punta a una struttura [**\_ PARAMS NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) che contiene informazioni che un'applicazione può usare per calcolare le nuove dimensioni e posizione del rettangolo client.

Se *wParam* è **FALSE,** *lParam* punta a una [**struttura RECT.**](/previous-versions//dd162897(v=vs.85)) All'immissione, la struttura contiene il rettangolo della finestra proposto per la finestra. In uscita, la struttura deve contenere le coordinate dello schermo dell'area client della finestra corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se il *parametro wParam* è **FALSE,** l'applicazione deve restituire zero.

Se *wParam* è **TRUE,** l'applicazione deve restituire zero o una combinazione dei valori seguenti.

Se *wParam* è **TRUE** e un'applicazione restituisce zero, l'area client precedente viene mantenuta e allineata all'angolo superiore sinistro della nuova area client.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_ ALIGNTOP**</dt> <dt>0x0010</dt> </dl>    | Specifica che l'area client della finestra deve essere mantenuta e allineata alla parte superiore della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo superiore sinistro, restituire i valori WVR ALIGNTOP e \_ **WVR \_ ALIGNLEFT.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_ ALIGNRIGHT**</dt> <dt>0x0080</dt> </dl>  | Specifica che l'area client della finestra deve essere mantenuta e allineata al lato destro della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo inferiore destro, restituire i valori **WVR \_ ALIGNRIGHT** e WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_ ALIGNLEFT**</dt> <dt>0x0020</dt> </dl>   | Specifica che l'area client della finestra deve essere mantenuta e allineata al lato sinistro della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo inferiore sinistro, restituire i valori **WVR \_ ALIGNLEFT** e **WVR \_ ALIGNBOTTOM.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_ ALIGNBOTTOM**</dt> <dt>0x0040</dt> </dl> | Specifica che l'area client della finestra deve essere mantenuta e allineata alla parte inferiore della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo superiore sinistro, restituire i valori WVR ALIGNTOP e \_ **WVR \_ ALIGNLEFT.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_ HREDRAW**</dt> <dt>0x0100</dt> </dl>     | Usato in combinazione con qualsiasi altro valore, ad eccezione di **WVR \_ VALIDRECTS,** fa sì che la finestra venga completamente ridisegnata se le dimensioni del rettangolo client cambiano orizzontalmente. Questo valore è simile allo stile [della \_ classe CS HREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_ VREDRAW**</dt> <dt>0x0200</dt> </dl>     | Usato in combinazione con qualsiasi altro valore, ad eccezione di **WVR \_ VALIDRECTS,** fa sì che la finestra venga completamente ridisegnata se le dimensioni del rettangolo client cambiano verticalmente. Questo valore è simile allo stile [della \_ classe CS VREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ RIDISEGNA**</dt> <dt>0x0300</dt> </dl>      | Questo valore determina il ridisegno dell'intera finestra. Si tratta di una combinazione **di valori WVR \_ HREDRAW** **e WVR \_ VREDRAW.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_ VALIDRECTS**</dt> <dt>0x0400</dt> </dl>  | Questo valore indica che, al ritorno da [**WM \_ NCCALCSIZE,**](wm-nccalcsize.md)i rettangoli specificati dai membri **rgrc** 1 e \[ \] **rgrc** 2 della struttura \[ \] [**\_ PARAMS NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) contengono rispettivamente rettangoli di destinazione e di area di origine validi. Il sistema combina questi rettangoli per calcolare l'area della finestra da mantenere. Il sistema copia qualsiasi parte dell'immagine della finestra all'interno del rettangolo di origine e ritaglia l'immagine nel rettangolo di destinazione. Entrambi i rettangoli sono in coordinate padre-relative o relative dello schermo. Questo flag non può essere combinato con altri flag. <br/> Questo valore restituito consente a un'applicazione di implementare strategie di conservazione dell'area client più elaborate, ad esempio centrare o mantenere un subset dell'area client.<br/> |



 

## <a name="remarks"></a>Commenti

La finestra può essere ridisegnata, a seconda che sia specificato lo stile di classe [CS \_ HREDRAW](about-window-classes.md) o CS \_ VREDRAW. Si tratta dell'elaborazione predefinita compatibile con le versioni precedenti di questo messaggio da parte della funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (oltre al consueto calcolo del rettangolo client descritto nella tabella precedente).

Quando *wParam* è **TRUE,** la semplice restituzione di 0 senza elaborare i rettangoli [**\_ PARAMS NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) causerà il ridimensionamento dell'area client alle dimensioni della finestra, inclusa la cornice della finestra. In questo modo la cornice della finestra e gli elementi didascalia verranno eliminati dalla finestra, lasciando visualizzata solo l'area client.

A partire da Windows Vista, la rimozione del frame standard semplicemente restituisce 0 quando *wParam* è **TRUE** non influisce sui frame estesi nell'area client usando la funzione [**DwmExtendFrameIntoClientArea.**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) Verrà rimosso solo il frame standard.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Movewindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**Setwindowpos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**NCCALCSIZE \_ PARAMS**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
