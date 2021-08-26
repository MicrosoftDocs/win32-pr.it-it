---
title: WM_GETDLGCODE messaggio (Winuser.h)
description: Inviato alla routine della finestra associata a un controllo .
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- WM_GETDLGCODE finestre di dialogo del messaggio
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
ms.openlocfilehash: 10d9ef69c2a6e89154cd6d931e05f9e52b4c51b214319bca8dffa9f86786a3da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022191"
---
# <a name="wm_getdlgcode-message"></a>Messaggio WM \_ GETDLGCODE

Inviato alla routine della finestra associata a un controllo . Per impostazione predefinita, il sistema gestisce tutto l'input da tastiera per il controllo. il sistema interpreta determinati tipi di input da tastiera come tasti di spostamento della finestra di dialogo. Per eseguire l'override di questo comportamento predefinito, il controllo può rispondere al **messaggio WM \_ GETDLGCODE** per indicare i tipi di input che vuole elaborare.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tasto virtuale, premuto dall'utente, che ha Windows di inviare questa notifica. Il gestore deve gestire in modo selettivo queste chiavi. Ad esempio, il gestore potrebbe accettare ed elaborare **VK \_ RETURN,** ma delegare **la scheda VK \_** alla finestra proprietaria. Per un elenco di valori, vedere [**Codici chiave virtuale**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) (o **NULL** se il sistema esegue una query).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno o più dei valori seguenti, che indicano il tipo di input che l'applicazione elabora.



| Codice/valore restituito                                                                                                                                                | Descrizione                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ PULSANTE**</dt> <dt>0x2000</dt> </dl>          | Pulsante.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Pulsante di push predefinito.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**EM \_ Messaggi SETSEL.**](/windows/desktop/Controls/em-setsel)<br/>                                                           |
| <dl> <dt>**DLGC \_ CONTROLLO RADIOBUTTON**</dt> <dt>0x0040</dt> </dl>     | Pulsante di opzione.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_ 0x0100**</dt> <dt></dt> </dl>          | Controllo statico.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UnDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | Pulsante di push non predefinito.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | Tutti gli input da tastiera.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt> </dl>      | Tasti di direzione.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt> </dl>       | [**WM \_ Messaggi CHAR.**](/windows/desktop/inputdev/wm-char)<br/>                                                                      |
| <dl> <dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt> </dl>     | Tutto l'input da tastiera (l'applicazione passa questo messaggio nella [**struttura MSG**](/windows/win32/api/winuser/ns-winuser-msg) al controllo).<br/> |
| <dl> <dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt> </dl>         | TASTO TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Commenti

Anche se la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce sempre zero in risposta al messaggio **WM \_ GETDLGCODE,** la routine della finestra per le classi di controllo predefinite restituisce un codice appropriato per ogni classe.

Il **messaggio WM \_ GETDLGCODE** e i valori restituiti sono utili solo con i controlli della finestra di dialogo definiti dall'utente o i controlli standard modificati dalla sottoclasse.

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

[**EM \_ SETSEL**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**Msg**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

