---
description: È possibile ruotare i tipi di carattere TrueType in qualsiasi angolo.
ms.assetid: 371ddb04-410a-425b-857f-ed3d4749b0f9
title: Rotazione di righe di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703dd4543caaa083d0b2d66512b53a0b5a213c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978295"
---
# <a name="rotating-lines-of-text"></a><span data-ttu-id="ccd75-103">Rotazione di righe di testo</span><span class="sxs-lookup"><span data-stu-id="ccd75-103">Rotating Lines of Text</span></span>

<span data-ttu-id="ccd75-104">È possibile ruotare i tipi di carattere TrueType in qualsiasi angolo.</span><span class="sxs-lookup"><span data-stu-id="ccd75-104">You can rotate TrueType fonts at any angle.</span></span> <span data-ttu-id="ccd75-105">Questa operazione è utile per l'assegnazione di etichette a grafici e altre illustrazioni.</span><span class="sxs-lookup"><span data-stu-id="ccd75-105">This is useful for labeling charts and other illustrations.</span></span> <span data-ttu-id="ccd75-106">Nell'esempio seguente viene ruotata una stringa in incrementi di 10 gradi intorno al centro dell'area client modificando il valore dei membri **lfEscapement** e **LfOrientation** della struttura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) utilizzata per creare il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ccd75-106">The following example rotates a string in 10-degree increments around the center of the client area by changing the value of the **lfEscapement** and **lfOrientation** members of the [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure used to create the font.</span></span>


```C++
#include "strsafe.h"
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    
    case WM_PAINT:
        {
        hdc = BeginPaint(hWnd, &ps);
        RECT rc; 
        int angle; 
        HGDIOBJ hfnt, hfntPrev; 
        WCHAR lpszRotate[22] = TEXT("String to be rotated.");
        HRESULT hr; 
        size_t pcch = 22;
 
// Allocate memory for a LOGFONT structure. 
 
PLOGFONT plf = (PLOGFONT) LocalAlloc(LPTR, sizeof(LOGFONT)); 
 
 
// Specify a font typeface name and weight. 
 
hr = StringCchCopy(plf->lfFaceName, 6, TEXT("Arial"));
if (FAILED(hr))
{
// TODO: write error handler
}

plf->lfWeight = FW_NORMAL; 
 
// Retrieve the client-rectangle dimensions. 
 
GetClientRect(hWnd, &rc); 
 
// Set the background mode to transparent for the 
// text-output operation. 
 
SetBkMode(hdc, TRANSPARENT); 
 
// Draw the string 36 times, rotating 10 degrees 
// counter-clockwise each time. 
 
for (angle = 0; angle < 3600; angle += 100) 
{ 
    plf->lfEscapement = angle; 
    hfnt = CreateFontIndirect(plf); 
    hfntPrev = SelectObject(hdc, hfnt);
    
    //
    // The StringCchLength call is fitted to the lpszRotate string
    //
    hr = StringCchLength(lpszRotate, 22, &pcch);
    if (FAILED(hr))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, rc.right / 2, rc.bottom / 2, 
        lpszRotate, pcch); 
    SelectObject(hdc, hfntPrev); 
    DeleteObject(hfnt); 
} 
 
// Reset the background mode to its default. 
 
SetBkMode(hdc, OPAQUE); 
 
// Free the memory allocated for the LOGFONT structure. 
 
LocalFree((LOCALHANDLE) plf); 
        EndPaint(hWnd, &ps);
        break;
        }
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



