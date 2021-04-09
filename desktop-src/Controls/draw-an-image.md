---
title: Come creare un'immagine
description: Questo argomento illustra come usare la funzione di creazione ImageList \_ per creare un'immagine.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963592"
---
# <a name="how-to-draw-an-image"></a><span data-ttu-id="ad97d-103">Come creare un'immagine</span><span class="sxs-lookup"><span data-stu-id="ad97d-103">How to Draw an Image</span></span>

<span data-ttu-id="ad97d-104">Questo argomento illustra come usare la funzione di creazione [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per creare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="ad97d-104">This topic demonstrates how to use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ad97d-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="ad97d-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ad97d-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="ad97d-106">Technologies</span></span>

-   [<span data-ttu-id="ad97d-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="ad97d-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ad97d-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="ad97d-108">Prerequisites</span></span>

-   <span data-ttu-id="ad97d-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="ad97d-109">C/C++</span></span>
-   <span data-ttu-id="ad97d-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="ad97d-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ad97d-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="ad97d-111">Instructions</span></span>


<span data-ttu-id="ad97d-112">Per creare un'immagine, è possibile usare la funzione [**ImageList \_ disegnato**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) .</span><span class="sxs-lookup"><span data-stu-id="ad97d-112">To draw an image, you use the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) or [**ImageList\_DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) function.</span></span> <span data-ttu-id="ad97d-113">È possibile specificare l'handle per un elenco di immagini, l'indice dell'immagine da disegnare, l'handle per il contesto di dispositivo di destinazione, una posizione all'interno del contesto di dispositivo e uno o più stili di disegno.</span><span class="sxs-lookup"><span data-stu-id="ad97d-113">You specify the handle to an image list, the index of the image to draw, the handle to the destination device context, a location within the device context, and one or more drawing styles.</span></span>

<span data-ttu-id="ad97d-114">La funzione definita dall'utente nell'esempio di codice C++ seguente usa la funzione di creazione [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per creare un'immagine e salva le coordinate client del rettangolo di delimitazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="ad97d-114">The user-defined function in the following C++ code example uses the [**ImageList\_Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) function to draw an image and saves the client coordinates of the image's bounding rectangle.</span></span> <span data-ttu-id="ad97d-115">Una funzione successiva usa il rettangolo di delimitazione per determinare se l'utente ha fatto clic sull'immagine.</span><span class="sxs-lookup"><span data-stu-id="ad97d-115">A subsequent function uses the bounding rectangle to determine whether the user has clicked on the image.</span></span>



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="ad97d-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad97d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad97d-117">Informazioni di riferimento sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="ad97d-117">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="ad97d-118">Informazioni sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="ad97d-118">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="ad97d-119">Uso degli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="ad97d-119">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




