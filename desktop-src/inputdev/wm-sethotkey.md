---
title: Messaggio WM_SETHOTKEY (winuser. h)
description: Inviato a una finestra per associare un tasto di scelta con la finestra. Quando l'utente preme il tasto di scelta, il sistema attiva la finestra.
ms.assetid: b2c7e6ca-da71-440b-a05e-17f2da419d18
keywords:
- Input della tastiera e del mouse WM_SETHOTKEY messaggio
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
ms.openlocfilehash: f7ed27a91ddf9506cd12b988db4bd141a988c13e
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "103761513"
---
# <a name="wm_sethotkey-message"></a>\_Messaggio di SEHOTKEY WM

Inviato a una finestra per associare un tasto di scelta con la finestra. Quando l'utente preme il tasto di scelta, il sistema attiva la finestra.


```C++
#define WM_SETHOTKEY                    0x0032
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica il codice della chiave virtuale da associare alla finestra.

La parola più significativa può essere uno o più dei seguenti valori di CommCtrl. h.

L'impostazione di *wParam* su **null** rimuove il tasto di scelta associato a una finestra.



| Valore                                                                                                                                                                                                                         | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="HOTKEYF_ALT"></span><span id="hotkeyf_alt"></span><dl> <dt>**HOTKEYF \_ ALT**</dt> <dt>0x04</dt> </dl>             | ALT (tasto)<br/>      |
| <span id="HOTKEYF_CONTROL"></span><span id="hotkeyf_control"></span><dl> <dt>**HOTKEYF \_**</dt> <dt>0x02</dt> di controllo </dl> | Tasto CTRL<br/>     |
| <span id="HOTKEYF_EXT"></span><span id="hotkeyf_ext"></span><dl> <dt>**HOTKEYF \_**</dt> <dt>0x08</dt> EXT </dl>             | Chiave estesa<br/> |
| <span id="HOTKEYF_SHIFT"></span><span id="hotkeyf_shift"></span><dl> <dt>**HOTKEYF \_ MAIUSC**</dt> <dt>0x01</dt> </dl>       | Tasto MAIUSC<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è uno dei seguenti.



| Valore restituito                                                                  | Descrizione                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>-1</dt> </dl> | La funzione ha esito negativo. il tasto di scelta non è valido.<br/>                        |
| <dl> <dt>0</dt> </dl>  | La funzione ha esito negativo. la finestra non è valida.<br/>                         |
| <dl> <dt>1</dt> </dl>  | La funzione ha esito positivo e nessun'altra finestra ha lo stesso tasto di scelta.<br/>        |
| <dl> <dt>2</dt> </dl>  | La funzione ha esito positivo, ma un'altra finestra ha già lo stesso tasto di scelta.<br/> |



 

## <a name="remarks"></a>Commenti

Impossibile associare un tasto di scelta a una finestra figlio.

**VK \_** Il carattere di escape, **\_ lo spazio VK** e la **\_ Scheda VK** sono tasti di scelta rapida non validi.

Quando l'utente preme il tasto di scelta, il sistema genera un [**messaggio \_ WM SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) con *wParam* uguale a **SC \_ HotKey** e *lParam* uguale all'handle della finestra. Se questo messaggio viene passato a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), il sistema visualizzerà l'ultimo popup attivo della finestra (se esistente) o la finestra stessa (se non è presente alcuna finestra popup) in primo piano.

Una finestra può avere solo un tasto di scelta. Se alla finestra è già associato un tasto di scelta, il nuovo tasto di scelta sostituisce quello precedente. Se più di una finestra ha lo stesso tasto di scelta, la finestra attivata dal tasto di scelta è casuale.

Questi tasti di scelta rapida non sono correlati ai tasti di scelta rapida impostati da [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey).

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

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GEThotkey**](wm-gethotkey.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

