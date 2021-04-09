---
title: Come usare le aree di lavoro List-View
description: In questo argomento viene illustrato come utilizzare le aree di lavoro visualizzazione elenco. Le aree di lavoro sono aree virtuali rettangolari che possono essere usate per disporre gli elementi in un controllo List-visualizzazione.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044546"
---
# <a name="how-to-use-list-view-working-areas"></a><span data-ttu-id="09243-104">Come usare le aree di lavoro List-View</span><span class="sxs-lookup"><span data-stu-id="09243-104">How to Use List-View Working Areas</span></span>

<span data-ttu-id="09243-105">In questo argomento viene illustrato come utilizzare le aree di lavoro visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="09243-105">This topic demonstrates how to work with list-view working areas.</span></span> <span data-ttu-id="09243-106">Le aree di lavoro sono aree virtuali rettangolari che possono essere usate per disporre gli elementi in un controllo List-visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="09243-106">Working areas are rectangular virtual areas that can be used to arrange items in a list-vew control.</span></span> <span data-ttu-id="09243-107">Un'area di lavoro non è una finestra e non può avere un bordo visibile.</span><span class="sxs-lookup"><span data-stu-id="09243-107">A working area is not a window and cannot have a visible border.</span></span> <span data-ttu-id="09243-108">Per impostazione predefinita, il controllo elenco-visualizzazione non contiene aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="09243-108">By default, the list-view control has no working areas.</span></span> <span data-ttu-id="09243-109">Creando un'area di lavoro, è possibile creare un bordo vuoto a sinistra, in alto o a destra degli elementi o causare la visualizzazione di una barra di scorrimento orizzontale quando normalmente non ne esiste una.</span><span class="sxs-lookup"><span data-stu-id="09243-109">By creating a working area, you can create an empty border on the left, top, or right of the items or cause a horizontal scroll bar to be displayed when there normally would not be one.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="09243-110">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="09243-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="09243-111">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="09243-111">Technologies</span></span>

-   [<span data-ttu-id="09243-112">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="09243-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="09243-113">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="09243-113">Prerequisites</span></span>

-   <span data-ttu-id="09243-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="09243-114">C/C++</span></span>
-   <span data-ttu-id="09243-115">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="09243-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="09243-116">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="09243-116">Instructions</span></span>

### <a name="create-a-working-area"></a><span data-ttu-id="09243-117">Creare un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="09243-117">Create a Working Area</span></span>

<span data-ttu-id="09243-118">Nell'esempio di codice C++ riportato di seguito viene illustrato come creare un'area di lavoro con un bordo vuoto di 25 pixel sui lati superiore, sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="09243-118">The following C++ code example demonstrates how to create a working area with a 25-pixel empty border on its top, left, and right sides.</span></span>


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a><span data-ttu-id="09243-119">Creazione di più aree di lavoro</span><span class="sxs-lookup"><span data-stu-id="09243-119">Create Multiple Working Areas</span></span>

<span data-ttu-id="09243-120">Nell'esempio di codice C++ riportato di seguito viene illustrato come creare due aree di lavoro in un controllo.</span><span class="sxs-lookup"><span data-stu-id="09243-120">The following C++ code example demonstrates how to create two working areas in a control.</span></span> <span data-ttu-id="09243-121">Ogni area di lavoro utilizza circa la metà dell'area client ed è racchiusa da un bordo vuoto di 25 pixel.</span><span class="sxs-lookup"><span data-stu-id="09243-121">Each working area uses about half of the client area, and is surrounded by a 25-pixel empty border.</span></span>


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a><span data-ttu-id="09243-122">Determinare l'area di lavoro a cui appartiene un elemento</span><span class="sxs-lookup"><span data-stu-id="09243-122">Determine the Working Area to Which an Item Belongs</span></span>

<span data-ttu-id="09243-123">Un modo per determinare l'area di lavoro a cui appartiene un elemento consiste nell'eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="09243-123">One way to determine which working area an item belongs is to do the following:</span></span>

-   <span data-ttu-id="09243-124">Recuperare l'elenco di coordinate di tutte le aree di lavoro nel controllo elenco-visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="09243-124">Retrieve the list of coordinates of all of the working areas in the list-view control.</span></span>
-   <span data-ttu-id="09243-125">Recuperare le coordinate dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="09243-125">Retrieve the coordinates of the item.</span></span>
-   <span data-ttu-id="09243-126">Determinare se le coordinate dell'elemento si trovano all'interno delle coordinate di una delle aree di lavoro.</span><span class="sxs-lookup"><span data-stu-id="09243-126">Determine whether the item coordinates lie within the coordinates of one of the working areas.</span></span>

<span data-ttu-id="09243-127">La funzione definita dall'applicazione nell'esempio di codice C++ seguente restituisce l'indice dell'area di lavoro a cui appartiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="09243-127">The application-defined function in the following C++ code example returns the index of the working area to which the item belongs.</span></span> <span data-ttu-id="09243-128">Se la funzione ha esito negativo, restituisce – 1.</span><span class="sxs-lookup"><span data-stu-id="09243-128">If the function fails, it returns –1.</span></span> <span data-ttu-id="09243-129">Se la funzione ha esito positivo, ma l'elemento non si trova all'interno di alcuna area di lavoro, la funzione restituisce 0, perché tutti gli elementi che non si trovano all'interno di un'area di lavoro diventano automaticamente membri dell'area di lavoro zero.</span><span class="sxs-lookup"><span data-stu-id="09243-129">If the function succeeds, but the item is not inside any of the working areas, the function returns 0, because all items that are not inside a working area automatically become a member of working area zero.</span></span>


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a><span data-ttu-id="09243-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09243-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09243-131">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="09243-131">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="09243-132">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="09243-132">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="09243-133">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="09243-133">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




