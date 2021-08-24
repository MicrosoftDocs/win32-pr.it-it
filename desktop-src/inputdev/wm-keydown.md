---
title: WM_KEYDOWN messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema. Un tasto non di sistema è un tasto premuto quando il tasto ALT non viene premuto.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN messaggio Input tastiera e mouse
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
ms.openlocfilehash: 9f54d0cad58a378d12247127d1ed70ab48653e18f4cceeb3c801efcf2aaae66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717201"
---
# <a name="wm_keydown-message"></a>Messaggio \_ WM KEYDOWN

Inviato alla finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema. Un tasto non di sistema è un tasto premuto quando il tasto ALT non viene premuto.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice della chiave virtuale della chiave non di sistema. Vedere [Codici di chiave virtuale](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Il numero di ripetizioni, il codice di analisi, il flag della chiave estesa, il codice di contesto, il flag di stato della chiave precedente e il flag di stato di transizione, come illustrato di seguito.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico a causa del fatto che l'utente tiene premuto il tasto. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se è una chiave estesa. in caso contrario, è 0.                                                              |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è sempre 0 per un **messaggio WM \_ KEYDOWN.**                                                                                                                                                                                                |
| 30    | Stato della chiave precedente. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è zero se la chiave è in alto.                                                                                                                                                 |
| 31    | Stato della transizione. Il valore è sempre 0 per un **messaggio WM \_ KEYDOWN.**                                                                                                                                                                                            |

Per altre informazioni, vedere [Flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).
 

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

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) in GitHub.


## <a name="remarks"></a>Commenti

Se viene premuto il tasto F10, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta un flag interno. Quando **DefWindowProc** riceve il messaggio [**WM \_ KEYUP,**](wm-keyup.md) la funzione verifica se il flag interno è impostato e, in tal caso, invia un messaggio [**\_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello. Il **parametro \_ SYSCOMMAND WM** del messaggio è impostato su SC \_ KEYMENU.

A causa della funzionalità autorepeat, è possibile che venga pubblicato più di un messaggio **WM \_ KEYDOWN** prima che venga pubblicato un messaggio [**WM \_ KEYUP.**](wm-keyup.md) Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio **WM \_ KEYDOWN** indica la prima transizione verso il basso o una transizione verso il basso ripetuta.

Per le tastiere avanzate da 101 e 102 tasti, i tasti estesi sono i tasti ALT e CTRL di destra nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

Le applicazioni devono *passare wParam* [**a TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ CHAR**](wm-char.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

