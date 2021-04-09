---
title: Come aggiungere elementi e elementi secondari List-View
description: In questo argomento viene illustrato come aggiungere elementi e elementi secondari a un controllo visualizzazione elenco.
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b3d20008edc10fda810261427507c77e9cfe34
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118674"
---
# <a name="how-to-add-list-view-items-and-subitems"></a>Come aggiungere elementi e elementi secondari List-View

In questo argomento viene illustrato come aggiungere elementi e elementi secondari a un controllo visualizzazione elenco.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per aggiungere un elemento a un controllo visualizzazione elenco, un'applicazione deve prima definire una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e quindi inviare un messaggio [**\_ INSERTITEM INSERTITEM**](lvm-insertitem.md) , specificando l'indirizzo della struttura **LVITEM** . Se in un'applicazione viene utilizzata la visualizzazione report, è necessario fornire il testo dell'elemento secondario.

Nell'esempio di codice C++ seguente viene compilata una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e vengono aggiunti gli elementi della visualizzazione elenco tramite il messaggio [**\_ InsertItem InsertItem**](lvm-insertitem.md) o la corrispondente macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem). Poiché l'applicazione salva il proprio testo, specifica il \_ valore TEXTCALLBACK LPSTR per il membro **pszText** della struttura **LVITEM** . \_Se si specifica il valore TEXTCALLBACK di LPSTR, il controllo Invia un codice di notifica [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) alla finestra proprietaria ogni volta che è necessario visualizzare un elemento.


```C++
// InsertListViewItems: Inserts items into a list view. 
// hWndListView:        Handle to the list-view control.
// cItems:              Number of items to insert.
// Returns TRUE if successful, and FALSE otherwise.
BOOL InsertListViewItems(HWND hWndListView, int cItems)
{
    LVITEM lvI;

    // Initialize LVITEM members that are common to all items.
    lvI.pszText   = LPSTR_TEXTCALLBACK; // Sends an LVN_GETDISPINFO message.
    lvI.mask      = LVIF_TEXT | LVIF_IMAGE |LVIF_STATE;
    lvI.stateMask = 0;
    lvI.iSubItem  = 0;
    lvI.state     = 0;

    // Initialize LVITEM members that are different for each item.
    for (int index = 0; index < cItems; index++)
    {
        lvI.iItem  = index;
        lvI.iImage = index;
    
        // Insert items into the list.
        if (ListView_InsertItem(hWndListView, &lvI) == -1)
            return FALSE;
    }

    return TRUE;
}

// HandleWM_NOTIFY - Handles the LVN_GETDISPINFO notification code that is 
//         sent in a WM_NOTIFY to the list view parent window. The function 
//        provides display strings for list view items and subitems.
//
// lParam - The LPARAM parameter passed with the WM_NOTIFY message.
// rgPetInfo - A global array of structures, defined as follows:
//         struct PETINFO
//        {
//            TCHAR szKind[10];
//            TCHAR szBreed[50];
//            TCHAR szPrice[20];
//        };
//
//        PETINFO rgPetInfo[ ] = 
//        {
//            {TEXT("Dog"),  TEXT("Poodle"),     TEXT("$300.00")},
//            {TEXT("Cat"),  TEXT("Siamese"),    TEXT("$100.00")},
//            {TEXT("Fish"), TEXT("Angel Fish"), TEXT("$10.00")},
//            {TEXT("Bird"), TEXT("Parakeet"),   TEXT("$5.00")},
//            {TEXT("Toad"), TEXT("Woodhouse"),  TEXT("$0.25")},
//        };
//
void HandleWM_NOTIFY(LPARAM lParam)
{
    NMLVDISPINFO* plvdi;

    switch (((LPNMHDR) lParam)->code)
    {
        case LVN_GETDISPINFO:

            plvdi = (NMLVDISPINFO*)lParam;

            switch (plvdi->item.iSubItem)
            {
                case 0:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szKind;
                    break;
                      
                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;
                
                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;
                
                default:
                    break;
            }

        break;

    }
    // NOTE: In addition to setting pszText to point to the item text, you could 
    // copy the item text into pszText using StringCchCopy. For example:
    //
    // StringCchCopy(plvdi->item.pszText, 
    //                         plvdi->item.cchTextMax, 
    //                         rgPetInfo[plvdi->item.iItem].szKind);

    return;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo visualizzazione elenco](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

 




