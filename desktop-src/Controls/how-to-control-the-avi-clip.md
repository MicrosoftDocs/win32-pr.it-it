---
title: Come controllare il clip AVI
description: In questo argomento viene illustrato come utilizzare le macro di controllo dell'animazione per riprodurre, arrestare e chiudere un clip di Audio-Video Interleaved (AVI) associato.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474705"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="ae42b-103">Come controllare il clip AVI</span><span class="sxs-lookup"><span data-stu-id="ae42b-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="ae42b-104">In questo argomento viene illustrato come utilizzare le macro di controllo dell'animazione per riprodurre, arrestare e chiudere un clip di Audio-Video Interleaved (AVI) associato.</span><span class="sxs-lookup"><span data-stu-id="ae42b-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ae42b-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="ae42b-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ae42b-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="ae42b-106">Technologies</span></span>

-   [<span data-ttu-id="ae42b-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="ae42b-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ae42b-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ae42b-108">Prerequisites</span></span>

-   <span data-ttu-id="ae42b-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ae42b-109">C/C++</span></span>
-   <span data-ttu-id="ae42b-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="ae42b-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="ae42b-111">File AVI</span><span class="sxs-lookup"><span data-stu-id="ae42b-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="ae42b-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ae42b-112">Instructions</span></span>


<span data-ttu-id="ae42b-113">Creare una funzione che accetta come parametri un handle per il controllo dell'animazione e un flag che indica l'azione da eseguire sul clip AVI associato.</span><span class="sxs-lookup"><span data-stu-id="ae42b-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="ae42b-114">La funzione nell'esempio C++ seguente chiama una delle tre macro del controllo di animazione ([**animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animate \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) in base al valore del parametro *nOutput azione* .</span><span class="sxs-lookup"><span data-stu-id="ae42b-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="ae42b-115">L'handle per il controllo dell'animazione associato al clip AVI viene passato tramite il parametro *hwndAnim* .</span><span class="sxs-lookup"><span data-stu-id="ae42b-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a><span data-ttu-id="ae42b-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae42b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae42b-117">Informazioni sui controlli di animazione</span><span class="sxs-lookup"><span data-stu-id="ae42b-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="ae42b-118">Riferimento al controllo Animation</span><span class="sxs-lookup"><span data-stu-id="ae42b-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ae42b-119">Uso di controlli di animazione</span><span class="sxs-lookup"><span data-stu-id="ae42b-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="ae42b-120">Controllo animazione</span><span class="sxs-lookup"><span data-stu-id="ae42b-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




