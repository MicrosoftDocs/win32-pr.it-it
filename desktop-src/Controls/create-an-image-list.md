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
# <a name="how-to-create-an-image-list"></a>Come creare un elenco di immagini

In questo argomento viene illustrato come utilizzare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) per creare un elenco di immagini.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per creare un elenco di immagini, chiamare la funzione [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . I parametri includono il tipo di elenco di immagini da creare, le dimensioni di ogni immagine e il numero di immagini che si desidera aggiungere all'elenco.

Nell'esempio seguente viene creato un elenco di immagini mascherate e viene utilizzata la macro [**\_ addicon di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) per aggiungere due icone all'elenco.



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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sugli elenchi di immagini](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informazioni sugli elenchi di immagini](image-lists.md)
</dt> <dt>

[Uso degli elenchi di immagini](using-image-lists.md)
</dt> </dl>

 

 




