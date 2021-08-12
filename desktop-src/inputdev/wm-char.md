---
title: WM_CHAR messaggio (Winuser.h)
description: Inviato alla finestra con lo stato attivo della tastiera quando un messaggio WM \_ KEYDOWN viene convertito dalla funzione TranslateMessage. Il messaggio WM \_ CHAR contiene il codice carattere del tasto premuto.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 16f9f1160f9766bd6284f62f2203b940ab6336f326aa31a0d9fa2894d243cf59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247950"
---
# <a name="wm_char-message"></a>Messaggio \_ WM CHAR

Inviato alla finestra con lo stato attivo della tastiera quando un [**messaggio WM \_ KEYDOWN**](wm-keydown.md) viene convertito dalla [**funzione TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) Il **messaggio WM \_ CHAR** contiene il codice carattere del tasto premuto.


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice carattere della chiave.

</dd> <dt>

*lParam* 
</dt> <dd>

Il conteggio delle ripetizioni, il codice di analisi, il flag di chiave estesa, il codice di contesto, il flag di stato della chiave precedente e il flag dello stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo automatico in seguito al fatto che l'utente tiene premuto il tasto. Se la pressione del tasto è sufficientemente lunga, vengono inviati più messaggi. Tuttavia, il conteggio delle ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se il tasto è un tasto esteso, ad esempio i tasti ALT e CTRL di destra visualizzati su una tastiera avanzata a 101 o 102 tasti. Il valore è 1 se si tratta di una chiave estesa. in caso contrario, è 0.                                                              |
| 25-28 | Riservato; non utilizzare .                                                                                                                                                                                                                                                 |
| 29    | Codice di contesto. Il valore è 1 se il tasto ALT viene premuto mentre viene premuto. In caso contrario, il valore è 0.                                                                                                                                                     |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave non è disponibile prima dell'invio del messaggio oppure è 0 se la chiave è in alto.                                                                                                                                                    |
| 31    | Stato della transizione. Il valore è 1 se il tasto viene rilasciato oppure è 0 se il tasto viene premuto.                                                                                                                                                            |

Per altri dettagli, vedere [Flag di messaggi di sequenza di tasti.](about-keyboard-input.md#keystroke-message-flags)
 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="example"></a>Esempio

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Il **messaggio WM \_ CHAR** usa il formato di trasformazione Unicode (UTF)-16.

Non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di caratteri generati, quindi le informazioni nella parola più importante del parametro *lParam* non sono in genere utili per le applicazioni. Le informazioni nella parola più importante si applicano solo al messaggio [**WM \_ KEYDOWN**](wm-keydown.md) più recente che precede la pubblicazione del **messaggio WM \_ CHAR.**

Per le tastiere avanzate a 101 e 102 tasti, i tasti estesi sono i tasti ALT destro e CTRL destro nella sezione principale della tastiera; i tasti INS, DEL, HOME, END, PGGIER, PGGI GIÙ e i tasti di direzione nei cluster a sinistra del tastierino numerico; e i tasti di divisione (/) e INVIO nel tastierino numerico. Altre tastiere possono supportare il bit del tasto esteso nel *parametro lParam.*

Il [**messaggio \_ WM UNICHAR**](wm-unichar.md) è identico a **WM \_ CHAR,** ad eccezione del fatto che usa UTF-32. È progettato per inviare o pubblicare caratteri Unicode nelle finestre ANSI e può gestire i caratteri del piano supplementare Unicode.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ UNICHAR**](wm-unichar.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

