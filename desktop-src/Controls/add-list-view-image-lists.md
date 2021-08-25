---
title: Come aggiungere elenchi List-View immagini
description: In questo argomento viene illustrato come aggiungere elenchi di immagini a un controllo visualizzazione elenco.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8875573634cd47fb5ccb271c3dabfca99daf9061469e31c1178b3e4ed938347e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922058"
---
# <a name="how-to-add-list-view-image-lists"></a>Come aggiungere elenchi List-View immagini

In questo argomento viene illustrato come aggiungere elenchi di immagini a un controllo visualizzazione elenco.

Si creano solo gli elenchi di immagini utilizzati dal controllo . Ad esempio, se l'applicazione non consente all'utente di passare alla visualizzazione icona, non è necessario creare e assegnare un elenco di icone di grandi dimensioni. Se si creano elenchi di immagini sia di grandi che di piccole dimensioni, questi devono contenere le stesse immagini nello stesso ordine, perché viene usato un singolo valore per identificare l'icona di un elemento di visualizzazione elenco in entrambi gli elenchi di immagini.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per visualizzare le immagini degli elementi, è necessario assegnare un elenco di immagini al controllo visualizzazione elenco. A tale scopo, usare il messaggio [**LVM \_ SETIMAGELIST**](lvm-setimagelist.md) o la macro [**corrispondente ListView \_ SetImageList,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist)specificando se l'elenco di immagini contiene icone a dimensione intera, icone piccole o immagini di stato. Per recuperare l'handle a un elenco di immagini attualmente assegnato a un controllo di visualizzazione elenco, usare il messaggio [**LVM \_ GETIMAGELIST.**](lvm-getimagelist.md) È possibile usare la [**funzione GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per determinare le dimensioni appropriate per le icone grandi e piccole.

Nell'esempio di codice C++ seguente la funzione definita dall'applicazione crea innanzitutto elenchi di immagini e quindi li assegna a un controllo visualizzazione elenco.


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View controlli](list-view-controls-overview.md)
</dt> <dt>

[Uso di List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 