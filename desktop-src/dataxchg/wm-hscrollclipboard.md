---
title: Messaggio WM_HSCROLLCLIPBOARD (winuser. h)
description: Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- Scambio di dati del messaggio WM_HSCROLLCLIPBOARD
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478304"
---
# <a name="wm_hscrollclipboard-message"></a>\_Messaggio HSCROLLCLIPBOARD WM

Inviato al proprietario degli Appunti da una finestra del visualizzatore degli Appunti. Questo errore si verifica quando gli Appunti contengono dati nel formato [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) e si verifica un evento nella barra di scorrimento orizzontale del visualizzatore degli Appunti. Il proprietario deve scorrere l'immagine degli Appunti e aggiornare i valori della barra di scorrimento.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra del visualizzatore degli Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore di *lParam* specifica un evento della barra di scorrimento. Questo parametro può avere uno dei valori seguenti. La parola più significativa di *lParam* specifica la posizione corrente della casella di scorrimento se la parola meno significativa di *lParam* è **SB \_ THUMBPOSITION**. in caso contrario, non viene usata la parola più significativa.



| Valore                                                                                                                                                                                                                         | Significato                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Fine scorrimento.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ SINISTRO**</dt> <dt>6</dt> </dl>                            | Scorrere fino alla parte superiore sinistra.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ DIRITTO**</dt> <dt>7</dt> </dl>                         | Scorrere in basso a destra.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> <dt>0</dt> </dl>                | Scorre verso sinistra di un'unità.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> <dt>1</dt> </dl>             | Scorre verso destra di un'unità.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> <dt>2</dt> </dl>                | Scorre verso sinistra in base alla larghezza della finestra.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ PAGERIGHT**</dt> <dt>3</dt> </dl>             | Scorre verso destra in base alla larghezza della finestra.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Scorrere fino alla posizione assoluta. La posizione corrente è specificata dalla parola più avanzata.<br/> |



 

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

 

