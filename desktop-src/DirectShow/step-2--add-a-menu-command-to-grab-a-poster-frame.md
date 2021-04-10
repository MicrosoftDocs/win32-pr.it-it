---
description: 'Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131890"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="88f6a-103">Passaggio 2: aggiungere un comando di menu per acquisire un frame di poster</span><span class="sxs-lookup"><span data-stu-id="88f6a-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="88f6a-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="88f6a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="88f6a-105">Questo argomento è il passaggio 2 dell' [acquisizione di un frame di poster](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="88f6a-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="88f6a-106">Successivamente, aggiungere un comando per l'utente per acquisire un frame di poster da un file.</span><span class="sxs-lookup"><span data-stu-id="88f6a-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="88f6a-107">Creare una voce di menu con un ID risorsa di \_ bitmap IDM e aggiungere l'istruzione case seguente alla routine della finestra:</span><span class="sxs-lookup"><span data-stu-id="88f6a-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



<span data-ttu-id="88f6a-108">La funzione DoShowBitmap restituirà il buffer allocato in *PBMI*.</span><span class="sxs-lookup"><span data-stu-id="88f6a-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="88f6a-109">Supponendo che la funzione abbia esito positivo, l'indirizzo della bitmap (</span><span class="sxs-lookup"><span data-stu-id="88f6a-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="88f6a-110">) può essere calcolato come offset da *PBMI*.</span><span class="sxs-lookup"><span data-stu-id="88f6a-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="88f6a-111">Nella funzione DoShowBitmap, visualizzare una finestra di dialogo **Apri file** che consente all'utente di scegliere un file e quindi chiamare la funzione GetBitmap definita dall'applicazione, che recupererà la bitmap:</span><span class="sxs-lookup"><span data-stu-id="88f6a-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



<span data-ttu-id="88f6a-112">[Passaggio 3: implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)</span><span class="sxs-lookup"><span data-stu-id="88f6a-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="88f6a-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88f6a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f6a-114">Acquisizione di un frame di poster</span><span class="sxs-lookup"><span data-stu-id="88f6a-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



