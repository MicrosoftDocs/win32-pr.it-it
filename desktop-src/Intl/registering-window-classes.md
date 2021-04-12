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
# <a name="registering-window-classes"></a><span data-ttu-id="27a4b-105">Registrazione di classi di finestre</span><span class="sxs-lookup"><span data-stu-id="27a4b-105">Registering Window Classes</span></span>

<span data-ttu-id="27a4b-106">Una classe di finestra è supportata da una routine di finestra.</span><span class="sxs-lookup"><span data-stu-id="27a4b-106">A window class is supported by a window procedure.</span></span> <span data-ttu-id="27a4b-107">L'applicazione può registrare una classe della finestra usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) o [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="27a4b-107">Your application can register a window class by using either [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa) or [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="27a4b-108">Le nuove applicazioni dovrebbero in genere usare **RegisterClassW**.</span><span class="sxs-lookup"><span data-stu-id="27a4b-108">New applications should typically use **RegisterClassW**.</span></span>

<span data-ttu-id="27a4b-109">Se l'applicazione registra la classe della finestra usando [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), la funzione informa il sistema operativo che la finestra della classe creata prevede che i messaggi con parametri di tipo text o character usino un set di caratteri della [tabella codici di Windows (ANSI)](code-pages.md) .</span><span class="sxs-lookup"><span data-stu-id="27a4b-109">If the application registers the window class using [**RegisterClassA**](/windows/win32/api/winuser/nf-winuser-registerclassa), the function informs the operating system that the windows of the created class expect messages with text or character parameters to use a [Windows (ANSI) code page](code-pages.md) character set.</span></span> <span data-ttu-id="27a4b-110">La registrazione tramite [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) consente all'applicazione di richiedere al sistema operativo di passare i parametri di testo dei messaggi come [Unicode](unicode.md).</span><span class="sxs-lookup"><span data-stu-id="27a4b-110">Registration using [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) allows the application to request the operating system to pass text parameters of messages as [Unicode](unicode.md).</span></span> <span data-ttu-id="27a4b-111">La funzione [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) consente a un'applicazione di eseguire una query sulla natura di ogni finestra.</span><span class="sxs-lookup"><span data-stu-id="27a4b-111">The [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) function enables an application to query the nature of each window.</span></span>

<span data-ttu-id="27a4b-112">Nell'esempio seguente viene illustrato come registrare una classe della finestra della tabella codici di Windows e una classe della finestra Unicode e come scrivere le routine della finestra per entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="27a4b-112">The following example shows how to register a Windows code page window class and a Unicode window class and how to write the window procedures for both cases.</span></span> <span data-ttu-id="27a4b-113">Ai fini di questo esempio, tutte le funzioni e tutte le strutture vengono visualizzate con i tipi di dati specifici "A" (ANSI) o "W" (Wide, Unicode).</span><span class="sxs-lookup"><span data-stu-id="27a4b-113">For the purposes of this example, all functions and structures are shown with the specific "A" (ANSI) or "W" (wide, Unicode) data types.</span></span> <span data-ttu-id="27a4b-114">Utilizzando le tecniche descritte in [utilizzo di tipi di dati generici](using-generic-data-types.md), in alternativa è possibile scrivere questo esempio per utilizzare tipi di dati generici, in modo che sia possibile compilare per utilizzare le tabelle codici di Windows o Unicode, a seconda che sia definito "Unicode".</span><span class="sxs-lookup"><span data-stu-id="27a4b-114">Using the techniques explained in [Using Generic Data Types](using-generic-data-types.md), you can alternatively write this example to use generic data types, so that it can be compiled to use either Windows code pages or Unicode, depending on whether "UNICODE" is defined.</span></span>


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



<span data-ttu-id="27a4b-115">Nell'esempio seguente viene illustrata la differenza tra la gestione del messaggio [**WM \_ char**](../inputdev/wm-char.md) in una procedura della finestra della tabella codici di Windows e una procedura di finestra Unicode.</span><span class="sxs-lookup"><span data-stu-id="27a4b-115">The following example shows the difference between handling the [**WM\_CHAR**](../inputdev/wm-char.md) message in a Windows code page window procedure and a Unicode window procedure.</span></span>


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



<span data-ttu-id="27a4b-116">Tutto il testo nei messaggi ricevuti da **AnsiWndProc** è costituito da caratteri della tabella codici di Windows.</span><span class="sxs-lookup"><span data-stu-id="27a4b-116">All text in messages received by **AnsiWndProc** is composed of Windows code page characters.</span></span> <span data-ttu-id="27a4b-117">Tutto il testo nei messaggi ricevuti da **uniwndproc** è costituito da caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="27a4b-117">All text in messages received by **UniWndProc** is composed of Unicode characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27a4b-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27a4b-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27a4b-119">Utilizzo di set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="27a4b-119">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
