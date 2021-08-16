---
title: WM_VSCROLLCLIPBOARD messaggio (Winuser.h)
description: Inviato al proprietario degli Appunti da una finestra del Visualizzatore Appunti quando gli Appunti contengono dati nel formato CF OWNERDISPLAY e si verifica un evento nella barra di scorrimento verticale del \_ visualizzatore Appunti.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD messaggio Data Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcf634870ce232543cd20ccd42c9e8ca255705810e81af39cc6e81f8e41658d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544876"
---
# <a name="wm_vscrollclipboard-message"></a>Messaggio \_ DI WM VSCROLLCLIPBOARD

Inviato al proprietario degli Appunti da una finestra del Visualizzatore Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e si verifica un evento nella barra di scorrimento verticale del visualizzatore Appunti. Il proprietario deve scorrere l'immagine degli Appunti e aggiornare i valori della barra di scorrimento.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore di *lParam* specifica un evento della barra di scorrimento. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                         | Significato                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> <dt>7</dt> </dl>                      | Scorrere verso il basso a destra.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Scorrimento finale.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Scorrere verso il basso di una riga.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> <dt>0</dt> </dl>                      | Scorrere una riga verso l'alto.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Scorrere una pagina verso il basso.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Scorrere di una pagina verso l'alto.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Scorrere fino alla posizione assoluta. La posizione corrente è specificata dalla parola più importante.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> <dt>6</dt> </dl>                               | Scorrere verso l'alto a sinistra.<br/>                                                                  |



 

La parola più alta di *lParam* specifica la posizione corrente della casella di scorrimento se la parola meno importante di *lParam* è **SB \_ THUMBPOSITION;** in caso contrario, la parola di ordine superiore *di lParam* non viene usata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il proprietario degli Appunti può usare la [**funzione ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) per scorrere l'immagine nella finestra del visualizzatore appunti e invalidare l'area appropriata.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

