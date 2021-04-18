---
description: Inviato quando è necessario calcolare le dimensioni e la posizione dell'area client di una finestra. Elaborando questo messaggio, un'applicazione può controllare il contenuto dell'area client della finestra quando cambiano le dimensioni o la posizione della finestra.
ms.assetid: d2d5825e-02a5-44b8-8615-55b7259d24ba
title: Messaggio WM_NCCALCSIZE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7d63fea3ad0a80bba686d8d86aa5354f0bb45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312369"
---
# <a name="wm_nccalcsize-message"></a>\_Messaggio NCCALCSIZE WM

Inviato quando è necessario calcolare le dimensioni e la posizione dell'area client di una finestra. Elaborando questo messaggio, un'applicazione può controllare il contenuto dell'area client della finestra quando cambiano le dimensioni o la posizione della finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCCALCSIZE                   0x0083
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Se *wParam* è **true**, specifica che l'applicazione deve indicare quale parte dell'area client contiene informazioni valide. Il sistema copia le informazioni valide nell'area specificata all'interno della nuova area client.

Se *wParam* è **false**, non è necessario che l'applicazione indichi la parte valida dell'area client.

</dd> <dt>

*lParam* 
</dt> <dd>

Se *wParam* è **true**, *lParam* punta a una struttura [**NCCALCSIZE \_ params**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) che contiene informazioni che possono essere utilizzate da un'applicazione per calcolare le nuove dimensioni e la posizione del rettangolo client.

Se *wParam* è **false**, *lParam* punta a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Alla voce, la struttura contiene il rettangolo della finestra proposto per la finestra. All'uscita, la struttura deve contenere le coordinate dello schermo dell'area client della finestra corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se il parametro *wParam* è **false**, l'applicazione deve restituire zero.

Se *wParam* è **true**, l'applicazione deve restituire zero o una combinazione dei valori seguenti.

Se *wParam* è **true** e un'applicazione restituisce zero, l'area client precedente viene mantenuta ed è allineata all'angolo superiore sinistro della nuova area client.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**WVR \_**</dt> <dt>0x0010</dt> ALIGNTOP </dl>    | Specifica che l'area client della finestra deve essere mantenuta e allineata con la parte superiore della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo superiore sinistro, restituire i \_ valori WVR ALIGNTOP e **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**WVR \_**</dt> <dt>0x0080</dt> ALIGNRIGHT </dl>  | Specifica che l'area client della finestra deve essere mantenuta e allineata con il lato destro della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo inferiore destro, restituire i valori **WVR \_ ALIGNRIGHT** e WVR \_ ALIGNBOTTOM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**WVR \_**</dt> <dt>0x0020</dt> ALIGNLEFT </dl>   | Specifica che l'area client della finestra deve essere mantenuta e allineata con il lato sinistro della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo inferiore sinistro, restituire i valori **WVR \_ ALIGNLEFT** e **WVR \_ ALIGNBOTTOM** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**WVR \_**</dt> <dt>0x0040</dt> ALIGNBOTTOM </dl> | Specifica che l'area client della finestra deve essere mantenuta e allineata con la parte inferiore della nuova posizione della finestra. Ad esempio, per allineare l'area client all'angolo superiore sinistro, restituire i \_ valori WVR ALIGNTOP e **WVR \_ ALIGNLEFT** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**WVR \_**</dt> <dt>0x0100</dt> HREDRAW </dl>     | Usato in combinazione con qualsiasi altro valore, ad eccezione di **WVR \_ VALIDRECTS**, fa sì che la finestra venga completamente ridisegnato se il rettangolo client cambia in orizzontale. Questo valore è simile allo stile della classe [cs \_ HREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**WVR \_**</dt> <dt>0x0200</dt> VREDRAW </dl>     | Usato in combinazione con qualsiasi altro valore, ad eccezione di **WVR \_ VALIDRECTS**, fa sì che la finestra venga completamente ridisegnato se il rettangolo client cambia in verticale. Questo valore è simile allo stile della classe [cs \_ VREDRAW](about-window-classes.md)<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**WVR \_ Ricreare**</dt> <dt>0x0300</dt> </dl>      | Questo valore causa il ridisegnato dell'intera finestra. Si tratta di una combinazione di valori **WVR \_ HREDRAW** e **WVR \_ VREDRAW** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**WVR \_**</dt> <dt>0x0400</dt> VALIDRECTS </dl>  | Questo valore indica che, al ritorno da [**WM \_ NCCALCSIZE**](wm-nccalcsize.md), i rettangoli specificati dai membri **rgrc** \[ 1 \] e **rgrc** \[ 2 \] della struttura [**\_ params di NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) contengono rispettivamente i rettangoli di area di destinazione e di origine validi. Il sistema combina questi rettangoli per calcolare l'area della finestra da mantenere. Il sistema copia qualsiasi parte dell'immagine della finestra che si trova all'interno del rettangolo di origine e ritaglia l'immagine nel rettangolo di destinazione. Entrambi i rettangoli si trovano in coordinate relative al padre o allo schermo. Questo flag non può essere combinato con altri flag. <br/> Questo valore restituito consente a un'applicazione di implementare strategie di conservazione dell'area client più elaborate, ad esempio il centramento o la conservazione di un subset dell'area client.<br/> |



 

## <a name="remarks"></a>Commenti

La finestra può essere ridisegnata, a seconda che lo stile della classe [cs \_ HREDRAW](about-window-classes.md) o cs \_ VREDRAW sia specificato. Si tratta dell'elaborazione predefinita compatibile con le versioni precedenti di questo messaggio tramite la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) (oltre al normale calcolo del rettangolo client descritto nella tabella precedente).

Quando *wParam* è **true**, la semplice restituzione di 0 senza elaborare i rettangoli dei [**\_ parametri NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params) comporterà il ridimensionamento dell'area client fino alla dimensione della finestra, inclusa la cornice della finestra. Questa operazione eliminerà la cornice della finestra e gli elementi della didascalia dalla finestra, lasciando visualizzata solo l'area client.

A partire da Windows Vista, rimuovendo il frame standard semplicemente restituendo 0 quando il valore *wParam* è **true** non influisce sui frame che vengono estesi nell'area client tramite la funzione [**DwmExtendFrameIntoClientArea**](/windows/win32/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) . Solo il frame standard verrà rimosso.

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

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[**\_parametri NCCALCSIZE**](/windows/win32/api/winuser/ns-winuser-nccalcsize_params)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
