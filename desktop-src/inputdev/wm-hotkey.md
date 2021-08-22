---
title: WM_HOTKEY messaggio (Winuser.h)
description: Pubblicato quando l'utente preme un tasto di scelta rapida registrato dalla funzione RegisterHotKey. Il messaggio viene inserito all'inizio della coda di messaggi associata al thread che ha registrato il tasto di scelta rapida.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dbd37b61fea12e559323a73cbf6b4a5cb54704a74663f865d9aa89636d3c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557141"
---
# <a name="wm_hotkey-message"></a>Messaggio WM \_ HOTKEY

Pubblicato quando l'utente preme un tasto di scelta rapida registrato dalla [**funzione RegisterHotKey.**](/windows/win32/api/winuser/nf-winuser-registerhotkey) Il messaggio viene inserito all'inizio della coda di messaggi associata al thread che ha registrato il tasto di scelta rapida.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del tasto di scelta rapida che ha generato il messaggio. Se il messaggio è stato generato da un tasto di scelta rapida definito dal sistema, questo parametro sarà uno dei valori seguenti.



| Valore                                                                                                                                                                                                                             | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | È stato premuto il tasto di scelta rapida "Blocca desktop".<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | È stato premuto il tasto di scelta rapida "finestra di agganciata".<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa specifica i tasti che dovevano essere premuti in combinazione con il tasto specificato dalla parola più alta per generare il **messaggio WM \_ HOTKEY.** Questa parola può essere uno o più dei valori seguenti. La parola più alta specifica il codice del tasto virtuale del tasto di scelta rapida.



| Valore                                                                                                                                                                                                               | Significato                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**MOD \_ ALT**</dt> <dt>0x0001</dt> </dl>             | È stato premuto il tasto ALT.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**MOD \_ Controllo**</dt> <dt>0x0002</dt> </dl> | È stato premuto il tasto CTRL.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**MOD \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>       | È stato premuto il tasto MAIUSC.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**MOD \_ Win**</dt> <dt>0x0008</dt> </dl>             | Il tasto WINDOWS è stato premuto. Queste chiavi sono etichettate con il logo Windows personalizzato. I tasti di scelta rapida che Windows chiave sono riservati per l'uso da parte del sistema operativo.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

**WM \_ HOTKEY** non è correlato ai tasti [**di scelta rapida WM \_ GETHOTKEY**](wm-gethotkey.md) e [**WM \_ SETHOTKEY.**](wm-sethotkey.md) Il **messaggio WM \_ HOTKEY viene** inviato per i tasti di scelta rapida generici, mentre i messaggi WM **\_ SETHOTKEY** e WM **\_ GETHOTKEY** sono correlati ai tasti di scelta rapida di attivazione della finestra.

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

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

