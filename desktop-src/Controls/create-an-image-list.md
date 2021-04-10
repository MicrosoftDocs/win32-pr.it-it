---
title: Come creare un elenco di immagini
description: In questo argomento viene illustrato come utilizzare la \_ funzione ImageList create per creare un elenco di immagini.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c81ff3a46138c210474a1b00ddd2ba647d1368
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963583"
---
# <a name="how-to-create-an-image-list"></a><span data-ttu-id="a466f-103">Come creare un elenco di immagini</span><span class="sxs-lookup"><span data-stu-id="a466f-103">How to Create an Image List</span></span>

<span data-ttu-id="a466f-104">In questo argomento viene illustrato come utilizzare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) per creare un elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="a466f-104">This topic demonstrates how to use the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function to create an image list.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a466f-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="a466f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a466f-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="a466f-106">Technologies</span></span>

-   [<span data-ttu-id="a466f-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="a466f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a466f-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="a466f-108">Prerequisites</span></span>

-   <span data-ttu-id="a466f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a466f-109">C/C++</span></span>
-   <span data-ttu-id="a466f-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="a466f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a466f-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="a466f-111">Instructions</span></span>


<span data-ttu-id="a466f-112">Per creare un elenco di immagini, chiamare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) .</span><span class="sxs-lookup"><span data-stu-id="a466f-112">You create an image list by calling the [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) function.</span></span> <span data-ttu-id="a466f-113">I parametri includono il tipo di elenco di immagini da creare, le dimensioni di ogni immagine e il numero di immagini che si desidera aggiungere all'elenco.</span><span class="sxs-lookup"><span data-stu-id="a466f-113">The parameters include the type of image list to create, the dimensions of each image, and the number of images that you intend to add to the list.</span></span>

<span data-ttu-id="a466f-114">Nell'esempio seguente viene creato un elenco di immagini mascherate e viene utilizzata la macro [**\_ addicon di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) per aggiungere due icone all'elenco.</span><span class="sxs-lookup"><span data-stu-id="a466f-114">The following example creates a masked image list and uses the [**ImageList\_AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) macro to add two icons to the list.</span></span>



```C++
// AddIconsToImageList - creates a masked image list and adds some 
// icons to it. 
// Returns the handle to the new image list. 
// hinst - handle to the application instance. 
// 
// Global variables and constants 
//     g_nBird and g_nTree - indexes of the images. 
//     cx_icon and cy_icon - width and height of the icon. 
//     num_icons - number of icons to add to the image list. 
extern int g_nBird, g_nTree; 
 
#define CX_ICON  32 
#define CY_ICON  32 
#define NUM_ICONS 3 
 
HIMAGELIST AddIconsToImageList(HINSTANCE hinst) 
{ 
    HIMAGELIST himlIcons;  // handle to new image list 
    HICON hicon;           // handle to icon 
 
    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Create a masked image list large enough to hold the icons. 
    himlIcons = ImageList_Create(CX_ICON, CY_ICON, ILC_MASK, NUM_ICONS, 0); 
 
    // Load the icon resources, and add the icons to the image list. 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_BIRD)); 
    g_nBird = ImageList_AddIcon(himlIcons, hicon); 
 
    hicon = LoadIcon(hinst, MAKEINTRESOURCE(IDI_TREE)); 
    g_nTree = ImageList_AddIcon(himlIcons, hicon); 
 
    return himlIcons; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="a466f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a466f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a466f-116">Informazioni di riferimento sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="a466f-116">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="a466f-117">Informazioni sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="a466f-117">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="a466f-118">Uso degli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="a466f-118">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 




