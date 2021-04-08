---
title: Come limitare lo spostamento del dispositivo di scorrimento
description: Come descritto in informazioni sui controlli TrackBar, è possibile impostare parte dell'intervallo TrackBar come intervallo di selezione. Uno degli scopi di un intervallo di selezione potrebbe essere quello di limitare lo spostamento del dispositivo di scorrimento, facendo in modo che alcune parti dell'intervallo completo non superino i limiti.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855706"
---
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="73d0d-104">Come limitare lo spostamento del dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="73d0d-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="73d0d-105">Come descritto in [informazioni sui controlli TrackBar](trackbar-controls.md), è possibile impostare parte dell'intervallo TrackBar come intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="73d0d-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="73d0d-106">Uno degli scopi di un intervallo di selezione potrebbe essere quello di limitare lo spostamento del dispositivo di scorrimento, facendo in modo che alcune parti dell'intervallo completo non superino i limiti.</span><span class="sxs-lookup"><span data-stu-id="73d0d-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="73d0d-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="73d0d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="73d0d-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="73d0d-108">Technologies</span></span>

-   [<span data-ttu-id="73d0d-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="73d0d-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="73d0d-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="73d0d-110">Prerequisites</span></span>

-   <span data-ttu-id="73d0d-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="73d0d-111">C/C++</span></span>
-   <span data-ttu-id="73d0d-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="73d0d-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="73d0d-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="73d0d-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="73d0d-114">Limita movimento dispositivo di scorrimento</span><span class="sxs-lookup"><span data-stu-id="73d0d-114">Limit Slider Movement</span></span>

<span data-ttu-id="73d0d-115">Il codice di esempio seguente limita lo spostamento del dispositivo di scorrimento reimpostando la posizione del dispositivo di scorrimento ogni volta che viene spostato al di fuori dell'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="73d0d-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a><span data-ttu-id="73d0d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="73d0d-116">Remarks</span></span>

<span data-ttu-id="73d0d-117">Questo frammento di codice fa parte di una procedura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="73d0d-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73d0d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73d0d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73d0d-119">Uso di controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="73d0d-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




