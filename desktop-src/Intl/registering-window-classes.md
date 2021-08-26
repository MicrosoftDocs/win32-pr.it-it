---
description: Una classe di finestra è supportata da una routine della finestra. L'applicazione può registrare una classe di finestra usando RegisterClassA o RegisterClassW. Le nuove applicazioni devono in genere usare RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrazione di classi di finestre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f508ebdbfa35f2551d723b3ef9a1ffd807917dfe71e503f9d77b2e8fdb136f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040451"
---
# <a name="registering-window-classes"></a>Registrazione di classi di finestre

Una classe di finestra è supportata da una routine della finestra. L'applicazione può registrare una classe di finestra usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW.**](/windows/win32/api/winuser/nf-winuser-registerclassa) Le nuove applicazioni devono in genere **usare RegisterClassW.**

Se l'applicazione registra la classe della finestra usando [**RegisterClassA,**](/windows/win32/api/winuser/nf-winuser-registerclassa)la funzione informa il sistema operativo che le finestre della classe creata prevedono l'uso di un set di caratteri della tabella codici [Windows (ANSI)](code-pages.md) per i messaggi con parametri di testo o carattere. La registrazione [**con RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) consente all'applicazione di richiedere al sistema operativo di passare i parametri di testo dei messaggi come [Unicode.](unicode.md) La [**funzione IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) consente a un'applicazione di eseguire query sulla natura di ogni finestra.

Nell'esempio seguente viene illustrato come registrare una Windows finestra della tabella codici e una classe finestra Unicode e come scrivere le routine della finestra per entrambi i casi. Ai fini di questo esempio, tutte le funzioni e le strutture vengono visualizzate con i tipi di dati "A" (ANSI) o "W" (wide, Unicode) specifici. Usando le tecniche illustrate in Uso di tipi di dati generici [,](using-generic-data-types.md)in alternativa è possibile scrivere questo esempio per usare tipi di dati generici, in modo che possa essere compilato per l'uso di una tabella codici Windows o Unicode, a seconda che sia definito o meno "UNICODE".


```C++
// Register a Windows code page window class.

WNDCLASSA AnsiWndCls;

AnsiWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
AnsiWndCls.lpfnWndProc   = (WNDPROC)AnsiWndProc;
AnsiWndCls.cbClsExtra    = 0;
AnsiWndCls.cbWndExtra    = 0;
AnsiWndCls.hInstance     = hInstance;
AnsiWndCls.hIcon         = NULL;
AnsiWndCls.hCursor       = LoadCursor(NULL, (LPTSTR)IDC_IBEAM);
AnsiWndCls.hbrBackground = NULL;
AnsiWndCls.lpszMenuName  = NULL;
AnsiWndCls.lpszClassName = "TestAnsi";

RegisterClassA(&AnsiWndCls);

// Register a Unicode window class.

WNDCLASSW UnicodeWndCls;

UnicodeWndCls.style         = CS_DBLCLKS | CS_PARENTDC;
UnicodeWndCls.lpfnWndProc   = (WNDPROC)UniWndProc;
UnicodeWndCls.cbClsExtra    = 0;
UnicodeWndCls.cbWndExtra    = 0;
UnicodeWndCls.hInstance     = hInstance;
UnicodeWndCls.hIcon         = NULL;
UnicodeWndCls.hCursor       = LoadCursor(NULL,(LPTSTR)IDC_IBEAM);
UnicodeWndCls.hbrBackground = NULL;
UnicodeWndCls.lpszMenuName  = NULL;
UnicodeWndCls.lpszClassName = L"TestUnicode";

RegisterClassW(&UnicodeWndCls);
```



Nell'esempio seguente viene illustrata la differenza tra la gestione del messaggio [**WM \_ CHAR**](../inputdev/wm-char.md) in una Windows routine della finestra della tabella codici e una routine della finestra Unicode.


```C++
// "ANSI" Window Procedure

LRESULT CALLBACK AnsiWndProc(HWND hWnd, UINT message,
                             WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpA("Q", (LPCSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

// Unicode Window Procedure

LRESULT CALLBACK UniWndProc(HWND hWnd, UINT message,
                            WPARAM wParam, LPARAM lParam)
{

    // Dispatch the messages that can be received.

    switch (message)
    {
        case WM_CHAR:

            // wParam - the value of the key
            // lParam - (not used in this example)

            if (lstrcmpW(L"Q", (LPCWSTR) wParam))
            {
                // ...
            }
            else
            {
                // ...
            }
            break;
        // Process other messages.
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



Tutto il testo nei messaggi ricevuti **da AnsiWndProc** è composto Windows caratteri della tabella codici. Tutto il testo nei messaggi ricevuti **da UniWndProc** è costituito da caratteri Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
