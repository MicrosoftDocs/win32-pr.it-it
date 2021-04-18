---
title: Uso di rettangoli (Windows Media Player SDK)
description: Uso di rettangoli
ms.assetid: b3fc16b4-dc93-43c0-a97d-5234e36437c8
keywords:
- Visualizzazioni, rettangoli
- Visualizzazioni personalizzate, rettangoli
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b48f16888d8e71c052d216a838683f2b7127e75
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300870"
---
# <a name="using-rectangles-windows-media-player-sdk"></a><span data-ttu-id="94d7a-108">Uso di rettangoli (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="94d7a-108">Using Rectangles (Windows Media Player SDK)</span></span>

<span data-ttu-id="94d7a-109">I rettangoli vengono utilizzati per specificare le aree rettangolari in Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="94d7a-109">Rectangles are used to specify rectangular areas in Microsoft Windows.</span></span> <span data-ttu-id="94d7a-110">È possibile creare molti rettangoli nella finestra, ma Windows Media Player fornisce i valori di un rettangolo tramite la funzione [IWMPEffects:: Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) .</span><span class="sxs-lookup"><span data-stu-id="94d7a-110">You can create many rectangles in your window, but Windows Media Player supplies the values of one rectangle through the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function.</span></span> <span data-ttu-id="94d7a-111">Se il plug-in viene eseguito tramite una finestra, il rettangolo è l'area client della finestra.</span><span class="sxs-lookup"><span data-stu-id="94d7a-111">If your plug-in renders using a window, the rectangle is the client area of the window.</span></span> <span data-ttu-id="94d7a-112">Questa operazione viene definita rettangolo PRC e definisce il rettangolo in cui verrà visualizzata la visualizzazione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="94d7a-112">This is called the prc rectangle, and it defines the rectangle that Windows Media Player will display your visualization through.</span></span> <span data-ttu-id="94d7a-113">Utilizzare questa frequenza per assicurarsi che non venga disegnato oltre gli extent del rettangolo fornito da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="94d7a-113">Use this frequently to be sure you do not draw beyond the extents of the rectangle supplied by Windows Media Player.</span></span>

<span data-ttu-id="94d7a-114">Un rettangolo ha quattro valori che lo definiscono.</span><span class="sxs-lookup"><span data-stu-id="94d7a-114">A rectangle has four values that define it.</span></span> <span data-ttu-id="94d7a-115">Sono a sinistra, in alto, a destra e in basso.</span><span class="sxs-lookup"><span data-stu-id="94d7a-115">They are left, top, right, and bottom.</span></span> <span data-ttu-id="94d7a-116">L'angolo superiore sinistro del rettangolo viene definito da Left e top, mentre l'angolo inferiore destro del rettangolo viene definito in basso e a destra.</span><span class="sxs-lookup"><span data-stu-id="94d7a-116">The top, left corner of the rectangle is defined by left and top, and the bottom, right corner of the rectangle is defined by bottom and right.</span></span>

<span data-ttu-id="94d7a-117">Usare il codice seguente per ottenere gli extent del rettangolo di disegno.</span><span class="sxs-lookup"><span data-stu-id="94d7a-117">Use the following code to get the extents of your drawing rectangle.</span></span> <span data-ttu-id="94d7a-118">È necessario eseguire questa operazione perché l'utente può ridimensionare la finestra e si vuole essere certi che il disegno venga sempre visualizzato in un'area che può essere visualizzata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="94d7a-118">You need to do this because the user may resize the window, and you want to be sure that you are always drawing in an area the user can see.</span></span>


```C++
int leftside = prc->left;
int rightside = prc->right;
int topside = prc->top;
int bottomside = prc->bottom;

```



<span data-ttu-id="94d7a-119">Per creare, ad esempio, da sinistra a destra, nella parte superiore della finestra, usare codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="94d7a-119">For example, to draw from left to right, along the top of the window, use code like this:</span></span>


```C++
::MoveToEx( hdc, prc->left, prc->top, NULL );  
::LineTo(hdc, prc->right, prc->top);

```



## <a name="related-topics"></a><span data-ttu-id="94d7a-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94d7a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94d7a-121">**Implementazione di rendering**</span><span class="sxs-lookup"><span data-stu-id="94d7a-121">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




