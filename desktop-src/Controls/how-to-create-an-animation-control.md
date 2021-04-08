---
title: Come creare un controllo di animazione
description: In questo argomento viene illustrato come creare un controllo di animazione.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044336"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="6965b-103">Come creare un controllo di animazione</span><span class="sxs-lookup"><span data-stu-id="6965b-103">How to Create an Animation Control</span></span>

<span data-ttu-id="6965b-104">In questo argomento viene illustrato come creare un controllo di animazione.</span><span class="sxs-lookup"><span data-stu-id="6965b-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="6965b-105">Nell'esempio di codice C++ associato viene creato un controllo Animation in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="6965b-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="6965b-106">Posiziona il controllo animazione sotto un controllo specificato e imposta le dimensioni del controllo animazione in base alle dimensioni di un frame nell'Audio-Video clip con interfoliazione (AVI).</span><span class="sxs-lookup"><span data-stu-id="6965b-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6965b-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="6965b-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6965b-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="6965b-108">Technologies</span></span>

-   [<span data-ttu-id="6965b-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="6965b-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6965b-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="6965b-110">Prerequisites</span></span>

-   <span data-ttu-id="6965b-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="6965b-111">C/C++</span></span>
-   <span data-ttu-id="6965b-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="6965b-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="6965b-113">File AVI</span><span class="sxs-lookup"><span data-stu-id="6965b-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="6965b-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="6965b-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="6965b-115">Passaggio 1: creare un'istanza del controllo Animation.</span><span class="sxs-lookup"><span data-stu-id="6965b-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="6965b-116">Utilizzare la macro [**animazione \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) per creare un'istanza del controllo Animation.</span><span class="sxs-lookup"><span data-stu-id="6965b-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="6965b-117">Passaggio 2: posizionare il controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="6965b-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="6965b-118">Ottiene le coordinate dello schermo del pulsante di controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="6965b-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="6965b-119">Converte le coordinate dell'angolo inferiore sinistro in coordinate client.</span><span class="sxs-lookup"><span data-stu-id="6965b-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="6965b-120">Posizionare il controllo animazione sotto il pulsante di controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="6965b-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="6965b-121">Passaggio 3: aprire il clip AVI.</span><span class="sxs-lookup"><span data-stu-id="6965b-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="6965b-122">Chiamare la macro [**\_ Apri animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) per aprire il clip AVI e visualizzare il primo fotogramma del controllo Animation.</span><span class="sxs-lookup"><span data-stu-id="6965b-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="6965b-123">Chiamare la funzione **ShowWindow** per rendere visibile il controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="6965b-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="6965b-124">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="6965b-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="6965b-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6965b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6965b-126">Informazioni sui controlli di animazione</span><span class="sxs-lookup"><span data-stu-id="6965b-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="6965b-127">Riferimento al controllo Animation</span><span class="sxs-lookup"><span data-stu-id="6965b-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6965b-128">Uso di controlli di animazione</span><span class="sxs-lookup"><span data-stu-id="6965b-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="6965b-129">Animazione</span><span class="sxs-lookup"><span data-stu-id="6965b-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




