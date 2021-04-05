---
description: Determina la lunghezza, in caratteri, del testo associato a una finestra.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Messaggio WM_GETTEXTLENGTH (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967923"
---
# <a name="wm_gettextlength-message"></a>\_Messaggio GETTEXTLENGTH WM

Determina la lunghezza, in caratteri, del testo associato a una finestra.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è la lunghezza del testo in caratteri, escluso il carattere null di terminazione.

## <a name="remarks"></a>Commenti

Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o del testo statico) della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per le altre finestre, il testo è il titolo della finestra. Per determinare la lunghezza di un elemento in una casella di riepilogo, un'applicazione può usare il messaggio [**\_ GETTEXTLEN lb**](../controls/lb-gettextlen.md) .

Quando viene inviato il messaggio **WM \_ GETTEXTLENGTH** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce la lunghezza, in caratteri, del testo. In determinate condizioni, la funzione **DefWindowProc** restituisce un valore maggiore della lunghezza effettiva del testo. Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è causata dal sistema che consente la presenza di caratteri DBCS (Double-byte character set) all'interno del testo. Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; è pertanto possibile utilizzarlo sempre per guidare l'allocazione del buffer. Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.

Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)o [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .

L'invio di un messaggio **WM \_ GETTEXTLENGTH** a un controllo statico non di testo, ad esempio una bitmap statica o un'icona statica controlc, non restituisce un valore stringa. Viene invece restituito zero.

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

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETtext**](wm-gettext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md)
</dt> <dt>

[**GetText LB \_**](../controls/lb-gettext.md)
</dt> <dt>

[**\_GETTEXTLEN lb**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
