---
title: Messaggio WM_KEYDOWN (winuser. h)
description: Inserito nella finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Input della tastiera e del mouse WM_KEYDOWN messaggio
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332667"
---
# <a name="wm_keydown-message"></a>\_Messaggio KeyDown di WM

Inserito nella finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave non di sistema. Vedere [codici chiave virtuale](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato della chiave precedente e il flag di stato di transizione, come illustrato di seguito.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il numero di ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è 0.                                                              |
| 25-28 | Riservati Non usare.                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è sempre 0 per un messaggio di un **\_ KeyDown di WM** .                                                                                                                                                                                                |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è zero se la chiave è attiva.                                                                                                                                                 |
| 31    | Stato di transizione. Il valore è sempre 0 per un messaggio di un **\_ KeyDown di WM** .                                                                                                                                                                                            |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="example"></a>Esempio

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) in GitHub.


## <a name="remarks"></a>Commenti

Se viene premuto il tasto F10, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta un flag interno. Quando **DefWindowProc** riceve il messaggio [**WM \_ KEYUP**](wm-keyup.md) , la funzione controlla se il flag interno è impostato e, in caso affermativo, invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello. Il parametro **WM \_ SYSCOMMAND** del messaggio viene impostato sul menu SC \_ .

A causa della funzionalità di ripetizione, è possibile che più di un messaggio **WM \_ KeyDown** venga pubblicato prima della pubblicazione di un messaggio [**WM \_ KEYUP**](wm-keyup.md) . Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio del **\_ KeyDown di WM** indica la prima transizione verso il basso o una transizione ripetuta verso il basso.

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .

Le applicazioni devono passare *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**\_carattere WM**](wm-char.md)
</dt> <dt>

[**KEYUP di WM \_**](wm-keyup.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

