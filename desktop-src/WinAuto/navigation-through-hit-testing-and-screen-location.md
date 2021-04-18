---
title: Navigazione tramite hit testing e posizione dello schermo
description: Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono colpire i punti di test sullo schermo.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298113"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="dd384-103">Navigazione tramite hit testing e posizione dello schermo</span><span class="sxs-lookup"><span data-stu-id="dd384-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="dd384-104">Per individuare gli elementi figlio di un oggetto o per determinare le dimensioni di un oggetto, i client possono colpire i punti di test sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="dd384-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="dd384-105">Sono disponibili due metodi:</span><span class="sxs-lookup"><span data-stu-id="dd384-105">Two methods are available:</span></span>

-   [<span data-ttu-id="dd384-106">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="dd384-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="dd384-107">**IAccessible:: accLocation**</span><span class="sxs-lookup"><span data-stu-id="dd384-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="dd384-108">Utilizzo di IAccessible:: accHitTest</span><span class="sxs-lookup"><span data-stu-id="dd384-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="dd384-109">Per determinare se un punto si trova all'interno di un oggetto, all'interno del relativo elemento figlio o nessuno dei due, i client chiamano il metodo [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) dell'oggetto padre, passando le coordinate dello schermo del punto da sottoporre a hit test.</span><span class="sxs-lookup"><span data-stu-id="dd384-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="dd384-110">Nell'elenco seguente vengono descritti alcuni scenari tipici:</span><span class="sxs-lookup"><span data-stu-id="dd384-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="dd384-111">Se gli elementi figlio dell'oggetto si sovrappongono in corrispondenza di un punto specificato, [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) Recupera il figlio più alto che sembra occupare lo spazio.</span><span class="sxs-lookup"><span data-stu-id="dd384-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="dd384-112">Se una finestra copre un elemento figlio o se l'elemento figlio viene ritagliato dall'elemento padre, l'hit testing del punto interessato recupera l'elemento figlio anche se non è visibile.</span><span class="sxs-lookup"><span data-stu-id="dd384-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="dd384-113">Se l'elemento figlio trovato in corrispondenza del punto specificato è un oggetto accessibile, anziché un elemento figlio, il metodo restituisce l'interfaccia [**IDispatch**](idispatch-interface.md) del figlio.</span><span class="sxs-lookup"><span data-stu-id="dd384-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="dd384-114">Utilizzo di IAccessible:: accLocation</span><span class="sxs-lookup"><span data-stu-id="dd384-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="dd384-115">Per ottenere la posizione dello schermo di un oggetto o di uno degli elementi figlio dell'oggetto, i client chiamano [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span><span class="sxs-lookup"><span data-stu-id="dd384-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="dd384-116">Questo metodo restituisce le coordinate del rettangolo di delimitazione dell'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="dd384-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="dd384-117">Se l'oggetto non ha una forma come un rettangolo, il metodo restituisce le coordinate del rettangolo più piccolo che include l'intero oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd384-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="dd384-118">La figura seguente mostra la relazione tra l'area dell'oggetto non rettangolare e il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="dd384-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![illustrazione che mostra un'area dell'oggetto non rettangolare (un cerchio) e il relativo rettangolo di delimitazione.](images/region.gif)

> [!Note]  
> <span data-ttu-id="dd384-120">[**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) è più preciso di [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) perché consente ai client di determinare la posizione degli oggetti in base al pixel anziché ai rettangoli di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="dd384-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="dd384-121">Questa precisione è utile, ad esempio, quando un'applicazione raccoglie informazioni monitorando la posizione del puntatore del mouse.</span><span class="sxs-lookup"><span data-stu-id="dd384-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




