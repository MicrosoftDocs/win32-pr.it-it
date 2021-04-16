---
description: "Passaggio 4: creare la bitmap nell'area client"
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: "Passaggio 4: creare la bitmap nell'area client"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401806"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="f4e14-103">Passaggio 4: creare la bitmap nell'area client</span><span class="sxs-lookup"><span data-stu-id="f4e14-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="f4e14-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f4e14-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f4e14-105">Questo argomento è il passaggio 4 dell' [acquisizione di un frame di poster](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="f4e14-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="f4e14-106">Il passaggio finale consiste nel creare la bitmap nell'area client della finestra dell'applicazione, usando la funzione [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) .</span><span class="sxs-lookup"><span data-stu-id="f4e14-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="f4e14-107">In questo esempio la bitmap viene semplicemente disegnata nell'angolo superiore sinistro dell'area client, indipendentemente dalle dimensioni della finestra:</span><span class="sxs-lookup"><span data-stu-id="f4e14-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="f4e14-108">Le variabili *pbuffer* e *PBMI* sono dichiarate nel [passaggio 1: creare il Framework Windows](step-1--create-the-windows-framework.md)e i relativi valori vengono ottenuti nel [passaggio 3: implementare la funzione Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).</span><span class="sxs-lookup"><span data-stu-id="f4e14-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4e14-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4e14-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4e14-110">Acquisizione di un frame di poster</span><span class="sxs-lookup"><span data-stu-id="f4e14-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
