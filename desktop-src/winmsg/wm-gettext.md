---
description: Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Messaggio WM_GETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757823"
---
# <a name="wm_gettext-message"></a>\_Messaggio WM GETtext

Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di caratteri da copiare, incluso il carattere null di terminazione.

Le applicazioni ANSI possono avere una dimensione del buffer ridotta (almeno metà del valore *wParam* ) a causa della conversione da ANSI a Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che deve ricevere il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Il valore restituito è il numero di caratteri copiati, escluso il carattere null di terminazione.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia il testo associato alla finestra nel buffer specificato e restituisce il numero di caratteri copiati. Si noti che, per i controlli statici non di testo, questo fornisce il testo con cui è stato originariamente creato il controllo, ovvero il numero ID. Tuttavia, fornisce l'ID del controllo statico non di testo creato in origine. Ovvero, se in seguito si utilizza un' **\_ Immagine STM** per modificarla, verrà comunque restituito l'ID originale.

Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica. Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o del testo statico) della casella combinata. Per un pulsante, il testo è il nome del pulsante. Per le altre finestre, il testo è il titolo della finestra. Per copiare il testo di un elemento in una casella di riepilogo, un'applicazione può usare il messaggio [**lb \_ gettext**](../controls/lb-gettext.md) .

Quando il messaggio **WM \_ gettext** viene inviato a un controllo statico con lo stile dell' **\_ icona SS** , viene restituito un handle per l'icona nei primi quattro byte del buffer a cui punta *lParam*. Questo vale solo se è stato usato il messaggio [**WM \_ SetText**](wm-settext.md) per impostare l'icona.

**Modifica avanzata:** Se il testo da copiare supera 64K, usare il messaggio em [**\_ Stream**](../controls/em-streamout.md) out o [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .

L'invio di un messaggio **WM \_ gettext** a un controllo statico non di testo, ad esempio una bitmap statica o un controllo icona statica, non restituisce un valore stringa. Viene invece restituito zero. Inoltre, nelle prime versioni di Windows, le applicazioni potevano inviare un messaggio **WM \_ gettext** a un controllo statico non di testo per recuperare l'ID del controllo. Per recuperare l'ID di un controllo, le applicazioni possono usare [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando l' **\_ ID GWL** come valore di indice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando l' **\_ ID GWLP**.

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

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**\_GETTEXTLENGTH WM**](wm-gettextlength.md)
</dt> <dt>

[**\_testo WM**](wm-settext.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_GETSELTEXT em**](../controls/em-getseltext.md)
</dt> <dt>

[**\_flusso em**](../controls/em-streamout.md)
</dt> <dt>

[**GetText LB \_**](../controls/lb-gettext.md)
</dt> </dl>

 

 
