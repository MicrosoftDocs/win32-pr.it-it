---
title: Messaggio WM_GETDLGCODE (winuser. h)
description: Inviato alla routine della finestra associata a un controllo.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Finestre di dialogo WM_GETDLGCODE messaggio
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302083"
---
# <a name="wm_getdlgcode-message"></a>\_Messaggio GETDLGCODE WM

Inviato alla routine della finestra associata a un controllo. Per impostazione predefinita, il sistema gestisce tutti gli input da tastiera al controllo; il sistema interpreta determinati tipi di input da tastiera come tasti di spostamento della finestra di dialogo. Per eseguire l'override di questo comportamento predefinito, il controllo può rispondere al messaggio **WM \_ GETDLGCODE** per indicare i tipi di input che desidera elaborare.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tasto virtuale, premuto dall'utente, che ha richiesto a Windows di emettere la notifica. Il gestore deve gestire in modo selettivo queste chiavi. Ad esempio, il gestore potrebbe accettare ed elaborare **la \_ restituzione VK** , ma delegare la **\_ Scheda VK** alla finestra proprietaria. Per un elenco di valori, vedere [**codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) (o **null** se il sistema sta eseguendo una query).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno o più dei valori seguenti, che indica il tipo di input elaborato dall'applicazione.



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ PULSANTE**</dt> <dt>0x2000</dt> </dl>          | Pulsante.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0010</dt> DEFPUSHBUTTON </dl>   | Pulsante di push predefinito.<br/>                                                                                            |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0008</dt> HASSETSEL </dl>       | [**Em \_ Messaggi SETSEL**](/windows/desktop/Controls/em-setsel) .<br/>                                                           |
| <dl> <dt>**DLGC \_ RADIOBUTTON**</dt> <dt>0x0040</dt> </dl>     | Pulsante di opzione.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0100</dt> statico </dl>          | Controllo statico.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0020</dt> UNDEFPUSHBUTTON </dl> | Pulsante di push non predefinito.<br/>                                                                                        |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0004</dt> WANTALLKEYS </dl>     | Tutti gli input da tastiera.<br/>                                                                                             |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0001</dt> WANTARROWS </dl>      | Tasti di direzione.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0080</dt> WANTCHARS </dl>       | [**WM \_ Messaggi CHAR**](/windows/desktop/inputdev/wm-char) .<br/>                                                                      |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0004</dt> WANTMESSAGE </dl>     | Tutti gli input da tastiera (l'applicazione passa questo messaggio nella struttura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) al controllo).<br/> |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0002</dt> WANTTAB </dl>         | Tasto TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Commenti

Sebbene la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisca sempre zero in risposta al messaggio **WM \_ GETDLGCODE** , la routine della finestra per le classi di controlli predefinite restituisce un codice appropriato per ogni classe.

Il messaggio **WM \_ GETDLGCODE** e i valori restituiti sono utili solo con i controlli della finestra di dialogo definiti dall'utente o i controlli standard modificati dalla sottoclasse.

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

[**\_SETSEL em**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**MESSAGGIO**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**\_carattere WM**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

