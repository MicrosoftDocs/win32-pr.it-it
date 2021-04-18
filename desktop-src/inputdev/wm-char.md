---
title: Messaggio WM_CHAR (winuser. h)
description: Inviato alla finestra con lo stato attivo quando un \_ messaggio di WM KeyDown viene convertito dalla funzione TranslateMessage. Il \_ messaggio WM Char contiene il codice carattere della chiave che è stata premuta.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Input della tastiera e del mouse WM_CHAR messaggio
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
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328281"
---
# <a name="wm_char-message"></a>\_Messaggio WM char

Inviato alla finestra con lo stato attivo quando un messaggio di [**WM \_ KeyDown**](wm-keydown.md) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Il messaggio **WM \_ char** contiene il codice carattere della chiave che è stata premuta.


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

Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.



| BITS  | Significato                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | Numero di ripetizioni per il messaggio corrente. Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente. Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi. Tuttavia, il numero di ripetizioni non è cumulativo. |
| 16-23 | Codice di analisi. Il valore dipende dall'OEM.                                                                                                                                                                                                                          |
| 24    | Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102. Il valore è 1 se è una chiave estesa; in caso contrario, è 0.                                                              |
| 25-28 | Riservati Non usare.                                                                                                                                                                                                                                                 |
| 29    | Codice del contesto. Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.                                                                                                                                                     |
| 30    | Stato precedente della chiave. Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.                                                                                                                                                    |
| 31    | Stato di transizione. Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.                                                                                                                                                            |

Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).
 

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
Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Il messaggio **WM \_ char** usa Unicode Transformation Format (UTF)-16.

Non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, quindi le informazioni nella parola più significativa del parametro *lParam* non sono in genere utili per le applicazioni. Le informazioni nella parola più ordinata si applicano solo al messaggio più recente di [**WM \_ KeyDown**](wm-keydown.md) che precede la pubblicazione del messaggio **WM \_ char** .

Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL destro nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico. È possibile che alcune altre tastiere supportino il bit della chiave estesa nel parametro *lParam* .

Il messaggio di [**WM \_ UNICHAR**](wm-unichar.md) è uguale a **WM \_ char**, ad eccezione del fatto che usa UTF-32. È progettato per inviare o inviare caratteri Unicode alle finestre ANSI e può gestire i caratteri del piano supplementare Unicode.

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**KeyDown di WM \_**](wm-keydown.md)
</dt> <dt>

[**UNICHAR WM \_**](wm-unichar.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

