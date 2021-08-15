---
title: WM_SETHOTKEY messaggio (Winuser.h)
description: Inviato a una finestra per associare un tasto di scelta rapida alla finestra. Quando l'utente preme il tasto di scelta rapida, il sistema attiva la finestra.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- WM_SETHOTKEY messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_SETHOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b6c9d4bdb4a59181fe3a413cca6861bc3663367cca9e7b34e0647de88978b0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482518"
---
# <a name="wm_sethotkey-message"></a>Messaggio WM \_ SETHOTKEY

Inviato a una finestra per associare un tasto di scelta rapida alla finestra. Quando l'utente preme il tasto di scelta rapida, il sistema attiva la finestra.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa specifica il codice della chiave virtuale da associare alla finestra.

La parola di ordine superiore può essere uno o più dei valori seguenti di CommCtrl.h.

*L'impostazione di wParam* **su NULL** rimuove il tasto di scelta rapida associato a una finestra.



| Valore                                                                                                                                                                                                                         | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>             | ALT (tasto)<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_ Controllo**</dt> <dt>0x02</dt> </dl> | TASTO CTRL<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_ EXT**</dt> <dt>0x08</dt> </dl>             | Chiave estesa<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ MAIUSC**</dt> <dt>0x01</dt> </dl>       | MAIUSC<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei seguenti.



| Valore restituito                                                                  | Descrizione                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | La funzione ha esito negativo. Il tasto di scelta rapida non è valido.<br/>                        |
| <dl> <dt>0</dt> </dl>  | La funzione ha esito negativo. la finestra non è valida.<br/>                         |
| <dl> <dt>1</dt> </dl>  | La funzione ha esito positivo e nessun'altra finestra ha lo stesso tasto di scelta rapida.<br/>        |
| <dl> <dt>2</dt> </dl>  | La funzione ha esito positivo, ma un'altra finestra ha già lo stesso tasto di scelta rapida.<br/> |



 

## <a name="remarks"></a>Commenti

Un tasto di scelta rapida non può essere associato a una finestra figlio.

**VK \_ ESCAPE,** **VK \_ SPACE e** **VK TAB \_ sono** tasti di scelta rapida non validi.

Quando l'utente preme il tasto di scelta rapida, il sistema genera un messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) con *wParam* uguale a **SC \_ HOTKEY** e *lParam* uguale all'handle della finestra. Se questo messaggio viene passato a [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)il sistema porta in primo piano l'ultimo popup attivo della finestra (se esistente) o la finestra stessa (se non è presente alcuna finestra popup).

Una finestra può avere un solo tasto di scelta rapida. Se alla finestra è già associato un tasto di scelta rapida, il nuovo tasto di scelta rapida sostituisce quello precedente. Se più di una finestra ha lo stesso tasto di scelta rapida, la finestra attivata dal tasto di scelta rapida è casuale.

Questi tasti di scelta rapida non sono correlati ai tasti di scelta rapida impostati [**da RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey)

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

