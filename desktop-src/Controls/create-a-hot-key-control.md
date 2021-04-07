---
title: Come creare un controllo tasto di scelta
description: In questo argomento viene illustrato come creare un controllo tasto di scelta. Per creare un controllo del tasto di scelta rapida, utilizzare la funzione CreateWindowEx, specificando la classe della finestra di scelta rapida \_ .
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873141"
---
# <a name="how-to-create-a-hot-key-control"></a><span data-ttu-id="c8f6e-104">Come creare un controllo tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="c8f6e-104">How to Create a Hot Key Control</span></span>

<span data-ttu-id="c8f6e-105">In questo argomento viene illustrato come creare un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-105">This topic demonstrates how to create a hot key control.</span></span> <span data-ttu-id="c8f6e-106">Per creare un controllo del tasto di scelta rapida, utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra di scelta rapida \_ .</span><span class="sxs-lookup"><span data-stu-id="c8f6e-106">You create a hot key control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the HOTKEY\_CLASS window class.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c8f6e-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c8f6e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c8f6e-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c8f6e-108">Technologies</span></span>

-   [<span data-ttu-id="c8f6e-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c8f6e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c8f6e-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c8f6e-110">Prerequisites</span></span>

-   <span data-ttu-id="c8f6e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c8f6e-111">C/C++</span></span>
-   <span data-ttu-id="c8f6e-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="c8f6e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c8f6e-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c8f6e-113">Instructions</span></span>


<span data-ttu-id="c8f6e-114">Prima di creare il controllo tasto di scelta, verificare che la DLL dei controlli comuni sia caricata.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-114">Before you create the hot key control, ensure that the common controls DLL is loaded.</span></span>

<span data-ttu-id="c8f6e-115">Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione chiama la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per caricare la dll del controllo comune.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-115">In the following C++ code example, the application-defined function calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="c8f6e-116">Chiama quindi la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra della **\_ classe hotkey** , per creare un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-116">Then it calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the **HOTKEY\_CLASS** window class, to create a hot key control.</span></span> <span data-ttu-id="c8f6e-117">USA i messaggi [**HKM \_**](hkm-setrules.md) e [**HKM \_ sehotkey**](hkm-sethotkey.md) per inizializzare il controllo e restituisce un handle per il controllo.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-117">It uses the [**HKM\_SETRULES**](hkm-setrules.md) and [**HKM\_SETHOTKEY**](hkm-sethotkey.md) messages to initialize the control and returns a handle to the control.</span></span>

<span data-ttu-id="c8f6e-118">Questo controllo tasto di scelta non consente all'utente di scegliere un tasto di scelta che è una singola chiave non modificata, né consente all'utente di scegliere solo MAIUSC e una chiave.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-118">This hot key control does not allow the user to choose a hot key that is a single unmodified key, nor does it permit the user to choose only SHIFT and a key.</span></span> <span data-ttu-id="c8f6e-119">Queste regole impediscono efficacemente all'utente di scegliere un tasto di scelta che potrebbe essere immesso accidentalmente durante la digitazione del testo.</span><span class="sxs-lookup"><span data-stu-id="c8f6e-119">These rules effectively prevent the user from choosing a hot key that might be entered accidentally while typing text.</span></span>



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a><span data-ttu-id="c8f6e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8f6e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8f6e-121">Riferimento al controllo del tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="c8f6e-121">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c8f6e-122">Informazioni sui controlli tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="c8f6e-122">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="c8f6e-123">Uso di controlli tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="c8f6e-123">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 