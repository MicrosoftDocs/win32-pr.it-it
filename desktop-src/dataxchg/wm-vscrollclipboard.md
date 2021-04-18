---
title: Messaggio WM_VSCROLLCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel \_ formato CF OWNERDISPLAY e si verifica un evento nella barra di scorrimento verticale del visualizzatore degli Appunti.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- Scambio di dati del messaggio WM_VSCROLLCLIPBOARD
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
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477176"
---
# <a name="wm_vscrollclipboard-message"></a>\_Messaggio VSCROLLCLIPBOARD WM

Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e si verifica un evento nella barra di scorrimento verticale del visualizzatore degli Appunti. Il proprietario deve scorrere l'immagine degli Appunti e aggiornare i valori della barra di scorrimento.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore degli Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore di *lParam* specifica un evento della barra di scorrimento. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                         | Significato                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ ULTIMI**</dt> <dt>7</dt> </dl>                      | Scorrere in basso a destra.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Fine scorrimento.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Scorrere una riga verso il basso.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> <dt>0</dt> </dl>                      | Scorre una riga verso l'alto.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PGGIÙ**</dt> <dt>3</dt> </dl>                | Scorrere una pagina verso il basso.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Scorrere una pagina verso l'alto.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Scorrere fino alla posizione assoluta. La posizione corrente è specificata dalla parola più avanzata.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ PRIMI**</dt> <dt>6</dt> </dl>                               | Scorrere fino alla parte superiore sinistra.<br/>                                                                  |



 

La parola più significativa di *lParam* specifica la posizione corrente della casella di scorrimento se la parola meno significativa di *lParam* è **SB \_ THUMBPOSITION**. in caso contrario, non viene usata la parola più ordinata di *lParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Il proprietario degli Appunti può utilizzare la funzione [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) per scorrere l'immagine nella finestra Visualizzatore Appunti e invalidare l'area appropriata.

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

 

