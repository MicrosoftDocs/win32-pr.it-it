---
description: Determina la lunghezza, in caratteri, del testo associato a una finestra.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: WM_GETTEXTLENGTH messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc01f6f7a2b74df41e97a84bb4d7e17d9c3e21966215fcbcca04222d1d5537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710391"
---
# <a name="wm_gettextlength-message"></a>Messaggio \_ WM GETTEXTLENGTH

Determina la lunghezza, in caratteri, del testo associato a una finestra.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è la lunghezza del testo in caratteri, senza includere il carattere Null di terminazione.

## <a name="remarks"></a>Commenti

Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o testo statico) della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per le altre finestre, il testo è il titolo della finestra. Per determinare la lunghezza di un elemento in una casella di riepilogo, un'applicazione può usare il messaggio [**\_ LB GETTEXTLEN.**](../controls/lb-gettextlen.md)

Quando viene **inviato il messaggio WM \_ GETTEXTLENGTH,** la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce la lunghezza, in caratteri, del testo. In determinate condizioni, **la funzione DefWindowProc** restituisce un valore maggiore della lunghezza effettiva del testo. Ciò si verifica con determinate combinazioni di ANSI e Unicode ed è dovuto al sistema che consente la possibile esistenza di caratteri DBCS (Double Byte Character Set) all'interno del testo. Il valore restituito, tuttavia, sarà sempre almeno quanto la lunghezza effettiva del testo. È quindi sempre possibile usarlo per guidare l'allocazione del buffer. Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e dialoghe comuni, che usano Unicode.

Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ GETTEXT**](wm-gettext.md), [**LB \_ GETTEXT**](../controls/lb-gettext.md)o [**\_ CB GETLBTEXT**](../controls/cb-getlbtext.md) o la [**funzione GetWindowText.**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)

L'invio di un messaggio **WM \_ GETTEXTLENGTH** a un controllo statico non di testo, ad esempio una bitmap statica o un controllo icona statica, non restituisce un valore stringa. Restituisce invece zero.

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

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> <dt>

[**LB \_ GETTEXTLEN**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
