---
title: Come creare un elenco di immagini
description: Questo argomento illustra come usare la funzione ImageList \_ Create per creare un elenco di immagini.
ms.assetid: 6092C555-B5B6-49DB-B07B-684EDB890761
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04e3e22894546e887e1a4ca5348518b4e4a35c45f4a26b5b6125b81f9323bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826481"
---
# <a name="how-to-create-an-image-list"></a>Come creare un elenco di immagini

Questo argomento illustra come usare la funzione [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) per creare un elenco di immagini.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per creare un elenco di immagini, chiamare la [**funzione ImageList \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) I parametri includono il tipo di elenco di immagini da creare, le dimensioni di ogni immagine e il numero di immagini che si intende aggiungere all'elenco.

Nell'esempio seguente viene creato un elenco di immagini mascherate e viene utilizzata la macro [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) per aggiungere due icone all'elenco.



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

[Informazioni di riferimento per gli elenchi di immagini](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informazioni sugli elenchi di immagini](image-lists.md)
</dt> <dt>

[Uso degli elenchi di immagini](using-image-lists.md)
</dt> </dl>

 

 




