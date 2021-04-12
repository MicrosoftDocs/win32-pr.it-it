---
description: Una classe di finestra è supportata da una routine di finestra. L'applicazione può registrare una classe della finestra usando RegisterClassA o RegisterClassW. Le nuove applicazioni dovrebbero in genere usare RegisterClassW.
ms.assetid: 016296ce-6151-4673-ad59-c69a2138a05a
title: Registrazione di classi di finestre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c82e9daead566e5bcb5419fccc234014005f6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132042"
---
# <a name="registering-window-classes"></a>Registrazione di classi di finestre

Una classe di finestra è supportata da una routine di finestra. L'applicazione può registrare una classe della finestra usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa). Le nuove applicazioni dovrebbero in genere usare **RegisterClassW**.

Se l'applicazione registra la classe della finestra usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la funzione informa il sistema operativo che la finestra della classe creata prevede che i messaggi con parametri di tipo text o character usino un set di caratteri della [tabella codici di Windows (ANSI)](code-pages.md) . La registrazione tramite [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) consente all'applicazione di richiedere al sistema operativo di passare i parametri di testo dei messaggi come [Unicode](unicode.md). La funzione [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) consente a un'applicazione di eseguire una query sulla natura di ogni finestra.

Nell'esempio seguente viene illustrato come registrare una classe della finestra della tabella codici di Windows e una classe della finestra Unicode e come scrivere le routine della finestra per entrambi i casi. Ai fini di questo esempio, tutte le funzioni e tutte le strutture vengono visualizzate con i tipi di dati specifici "A" (ANSI) o "W" (Wide, Unicode). Utilizzando le tecniche descritte in [utilizzo di tipi di dati generici](using-generic-data-types.md), in alternativa è possibile scrivere questo esempio per utilizzare tipi di dati generici, in modo che sia possibile compilare per utilizzare le tabelle codici di Windows o Unicode, a seconda che sia definito "Unicode".


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



Nell'esempio seguente viene illustrata la differenza tra la gestione del messaggio [**WM \_ char**](../inputdev/wm-char.md) in una procedura della finestra della tabella codici di Windows e una procedura di finestra Unicode.


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



Tutto il testo nei messaggi ricevuti da **AnsiWndProc** è costituito da caratteri della tabella codici di Windows. Tutto il testo nei messaggi ricevuti da **uniwndproc** è costituito da caratteri Unicode.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di set di caratteri e Unicode](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
