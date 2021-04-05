---
title: Come implementare le descrizioni comandi del fumetto
description: Le descrizioni comando a fumetti sono simili alle descrizioni comandi standard, ma vengono visualizzate in un fumetto \ 0034; Balloon \ 0034; con un gambo che punta allo strumento.
ms.assetid: 59FEA8B6-772D-4BEF-A18C-945EC6A56FA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe578f69092a35a7f3ccc5eaa6a5987128ebdd66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708668"
---
# <a name="how-to-implement-balloon-tooltips"></a><span data-ttu-id="3bd41-103">Come implementare le descrizioni comandi del fumetto</span><span class="sxs-lookup"><span data-stu-id="3bd41-103">How to Implement Balloon Tooltips</span></span>

<span data-ttu-id="3bd41-104">Le descrizioni comandi a fumetti sono simili alle descrizioni comandi standard, ma vengono visualizzate in un "fumetto" di tipo Cartoon con un gambo che punta allo strumento.</span><span class="sxs-lookup"><span data-stu-id="3bd41-104">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="3bd41-105">Le descrizioni comando a fumetti possono essere a riga singola o a più righe.</span><span class="sxs-lookup"><span data-stu-id="3bd41-105">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="3bd41-106">Vengono creati e gestiti in modo molto simile alle descrizioni comandi standard.</span><span class="sxs-lookup"><span data-stu-id="3bd41-106">They are created and handled in much the same way as standard tooltips.</span></span>

<span data-ttu-id="3bd41-107">La posizione predefinita del gambo e del rettangolo è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="3bd41-107">The default position of the stem and rectangle is shown in the following illustration.</span></span> <span data-ttu-id="3bd41-108">Se lo strumento è troppo vicino alla parte superiore dello schermo, la descrizione comando viene visualizzata sotto e a destra del rettangolo dello strumento.</span><span class="sxs-lookup"><span data-stu-id="3bd41-108">If the tool is too close to the top of the screen, the tooltip appears below and to the right of the tool's rectangle.</span></span> <span data-ttu-id="3bd41-109">Se lo strumento è troppo vicino al lato destro dello schermo, vengono applicati principi simili, ma la descrizione comando viene visualizzata a sinistra del rettangolo dello strumento.</span><span class="sxs-lookup"><span data-stu-id="3bd41-109">If the tool is too close to the right side of the screen, similar principles apply, but the tooltip appears to the left of the tool's rectangle.</span></span>

![Screenshot di una finestra di dialogo; una descrizione comando a fumetti con una riga di testo viene visualizzata sopra e a destra della destinazione](images/tt-balloon.png)

<span data-ttu-id="3bd41-111">È possibile modificare il posizionamento predefinito impostando il **flag \_ CENTERTIP di ttf** nel membro **uFlags** della struttura della descrizione comando [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3bd41-111">You can change the default positioning by setting the **TTF\_CENTERTIP** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="3bd41-112">In tal caso, il gambo punta normalmente al centro del bordo inferiore del rettangolo dello strumento e il rettangolo di testo viene visualizzato direttamente sotto lo strumento.</span><span class="sxs-lookup"><span data-stu-id="3bd41-112">In that case, the stem normally points to the center of the lower edge of the tool's rectangle, and the text rectangle is displayed directly below the tool.</span></span> <span data-ttu-id="3bd41-113">Il gambo si connette al rettangolo di testo al centro del bordo superiore.</span><span class="sxs-lookup"><span data-stu-id="3bd41-113">The stem attaches to the text rectangle at the center of the upper edge.</span></span> <span data-ttu-id="3bd41-114">Se lo strumento è troppo vicino alla parte inferiore dello schermo, il rettangolo di testo viene centrato sopra lo strumento e il gambo si connette al centro del bordo inferiore.</span><span class="sxs-lookup"><span data-stu-id="3bd41-114">If the tool is too close to the bottom of the screen, the text rectangle is centered above the tool, and the stem attaches to the center of the lower edge.</span></span>

<span data-ttu-id="3bd41-115">Nell'illustrazione seguente viene mostrata una descrizione comando centrata sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="3bd41-115">The following illustration shows a tooltip that is centered on the tool.</span></span>

![Screenshot di una finestra di dialogo; una descrizione comando a fumetti con una riga di testo viene visualizzata al centro sotto la destinazione](images/tt-ballooncenter.png)

<span data-ttu-id="3bd41-117">Se si vuole specificare dove si trova il punto di attacco, impostare il flag di **\_ traccia ttf** nel membro **UFlags** della struttura ToolTip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3bd41-117">If you want to specify where the stem points, set the **TTF\_TRACK** flag in the **uFlags** member of the tooltip [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="3bd41-118">Si specifica quindi la coordinata inviando un messaggio [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) con le coordinate x e y nel valore *lParam* .</span><span class="sxs-lookup"><span data-stu-id="3bd41-118">You then specify the coordinate by sending a [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message, with the x- and y-coordinates in the *lParam* value.</span></span> <span data-ttu-id="3bd41-119">Se si imposta anche **ttf \_ CENTERTIP** , il gambo fa ancora riferimento alla posizione specificata dal **messaggio \_ TRACKPOSITION di TTM** .</span><span class="sxs-lookup"><span data-stu-id="3bd41-119">If **TTF\_CENTERTIP** is also set, the stem still points to the position specified by the **TTM\_TRACKPOSITION** message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3bd41-120">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="3bd41-120">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3bd41-121">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="3bd41-121">Technologies</span></span>

-   [<span data-ttu-id="3bd41-122">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="3bd41-122">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3bd41-123">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3bd41-123">Prerequisites</span></span>

-   <span data-ttu-id="3bd41-124">C/C++</span><span class="sxs-lookup"><span data-stu-id="3bd41-124">C/C++</span></span>
-   <span data-ttu-id="3bd41-125">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="3bd41-125">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3bd41-126">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="3bd41-126">Instructions</span></span>

### <a name="implement-balloon-tooltips"></a><span data-ttu-id="3bd41-127">Implementare le descrizioni comandi del fumetto</span><span class="sxs-lookup"><span data-stu-id="3bd41-127">Implement Balloon Tooltips</span></span>

<span data-ttu-id="3bd41-128">Nell'esempio di codice riportato di seguito viene illustrato come implementare una descrizione comando a fumetti centrata utilizzando lo stile del controllo ToolTip di **sintesi vocale \_** .</span><span class="sxs-lookup"><span data-stu-id="3bd41-128">The following example code shows how to implement a centered balloon tooltip by using the **TTS\_BALLOON** tooltip control style.</span></span>


```C++
hwndToolTips = CreateWindow(TOOLTIPS_CLASS, NULL, 
                            WS_POPUP | TTS_NOPREFIX | TTS_BALLOON, 
                            0, 0, 0, 0, NULL, NULL, g_hinst, NULL);

if (hwndTooltip)
{
    TOOLINFO ti;

    ti.cbSize   = sizeof(ti);
    ti.uFlags   = TTF_TRANSPARENT | TTF_CENTERTIP;
    ti.hwnd     = hwnd;
    ti.uId      = 0;
    ti.hinst    = NULL;
    ti.lpszText = LPSTR_TEXTCALLBACK;

    GetClientRect(hwnd, &ti.rect);

    SendMessage(hwndToolTips, TTM_ADDTOOL, 0, (LPARAM) &ti );

}
            
```



## <a name="related-topics"></a><span data-ttu-id="3bd41-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bd41-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bd41-130">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="3bd41-130">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> <dt>

[<span data-ttu-id="3bd41-131">**Stili descrizione comando**</span><span class="sxs-lookup"><span data-stu-id="3bd41-131">**Tooltip Styles**</span></span>](tooltip-styles.md)
</dt> </dl>

 

 




