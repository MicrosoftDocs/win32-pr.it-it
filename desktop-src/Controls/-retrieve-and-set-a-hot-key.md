---
title: Come recuperare e impostare un tasto di scelta
description: In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300696"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="f6922-103">Come recuperare e impostare un tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="f6922-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="f6922-104">In questo argomento viene illustrato come recuperare o impostare la combinazione di tasti per un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="f6922-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="f6922-105">Il [**messaggio \_ sehotkey HKM**](hkm-sethotkey.md) consente a un'applicazione di impostare la combinazione di tasti di scelta rapida per un controllo tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="f6922-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="f6922-106">Le applicazioni utilizzano il messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare il codice della chiave virtuale e i flag di modifica del tasto di scelta rapida scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f6922-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f6922-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f6922-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f6922-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f6922-108">Technologies</span></span>

-   [<span data-ttu-id="f6922-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="f6922-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f6922-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f6922-110">Prerequisites</span></span>

-   <span data-ttu-id="f6922-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="f6922-111">C/C++</span></span>
-   <span data-ttu-id="f6922-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="f6922-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f6922-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f6922-113">Instructions</span></span>


<span data-ttu-id="f6922-114">Usare il [**messaggio \_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare il codice della chiave virtuale e i tasti di modifica che descrivono un tasto di scelta rapida scelto dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f6922-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="f6922-115">Usare il messaggio [**HKM \_ sehotkey**](hkm-sethotkey.md) per impostare i valori per un tasto di scelta.</span><span class="sxs-lookup"><span data-stu-id="f6922-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="f6922-116">Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione usa il messaggio [**\_ GetHotKey HKM**](hkm-gethotkey.md) per recuperare una combinazione di tasti da un controllo tasto di scelta rapida e quindi usa il messaggio per impostare un tasto di [**scelta rapida globale \_**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="f6922-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="f6922-117">Si noti che non è possibile impostare un tasto di scelta rapida globale per una finestra con lo stile della finestra [**\_ figlio WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="f6922-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="f6922-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6922-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6922-119">Riferimento al controllo del tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="f6922-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f6922-120">Informazioni sui controlli tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="f6922-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="f6922-121">Uso di controlli tasto di scelta</span><span class="sxs-lookup"><span data-stu-id="f6922-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 