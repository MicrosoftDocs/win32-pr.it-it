---
description: Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089891"
---
# <a name="wm_gettext-message"></a>Messaggio WM \_ GETTEXT

Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di caratteri da copiare, incluso il carattere Null di terminazione.

Le applicazioni ANSI possono avere la stringa nel buffer ridotta di dimensioni (almeno la metà di quella del *valore wParam)* a causa della conversione da ANSI a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che deve ricevere il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è il numero di caratteri copiati, senza includere il carattere Null di terminazione.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia il testo associato alla finestra nel buffer specificato e restituisce il numero di caratteri copiati. Si noti che, per i controlli statici non di testo, viene visualizzato il testo con cui è stato originariamente creato il controllo, ovvero il numero ID. Tuttavia, fornisce l'ID del controllo statico non di testo come creato in origine. Ciò significa che se successivamente è stata usata una **STM \_ SETIMAGE** per modificarlo, verrà comunque restituito l'ID originale.

Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o testo statico) della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per altre finestre, il testo è il titolo della finestra. Per copiare il testo di un elemento in una casella di riepilogo, un'applicazione può usare il [**messaggio \_ LB GETTEXT.**](../controls/lb-gettext.md)

Quando il **messaggio WM \_ GETTEXT** viene inviato a un controllo statico con lo stile **SS \_ ICON,** nei primi quattro byte del buffer a cui punta *lParam* verrà restituito un handle per l'icona . Questo vale solo se per impostare l'icona è stato usato il messaggio [**WM \_ SETTEXT.**](wm-settext.md)

**Rich Edit:** Se il testo da copiare supera 64.000, usare il messaggio [**EM \_ STREAMOUT**](../controls/em-streamout.md) o [**EM \_ GETSELTEXT.**](../controls/em-getseltext.md)

**L'invio di un messaggio WM \_ GETTEXT** a un controllo statico non di testo, ad esempio una bitmap statica o un controllo icona statica, non restituisce un valore stringa. Restituisce invece zero. Inoltre, nelle prime versioni di Windows, le applicazioni potrebbero inviare un messaggio **WM \_ GETTEXT** a un controllo statico non di testo per recuperare l'ID del controllo. Per recuperare l'ID di un controllo, le applicazioni possono usare [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando **\_ l'ID GWL** come valore di indice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando **\_ l'ID GWLP**.

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

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXTLENGTH**](wm-gettextlength.md)
</dt> <dt>

[**WM \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**EM \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**EM \_ STREAMOUT**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
