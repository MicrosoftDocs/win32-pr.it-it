---
title: Come aggiungere elementi List-View elementi secondari
description: In questo argomento viene illustrato come aggiungere elementi ed elementi secondari a un controllo visualizzazione elenco.
ms.assetid: B7E204DC-FD08-4639-985D-1459A1AC0ED6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6365e077c65da33424c5dadd32a0ab98ed6ab7c82eb83e1ecb5a3a007b0f27f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922041"
---
# <a name="how-to-add-list-view-items-and-subitems"></a>Come aggiungere elementi List-View elementi secondari

In questo argomento viene illustrato come aggiungere elementi ed elementi secondari a un controllo visualizzazione elenco.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per aggiungere un elemento a un controllo visualizzazione elenco, un'applicazione deve prima definire una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e quindi inviare un messaggio [**LVM \_ INSERTITEM,**](lvm-insertitem.md) specificando l'indirizzo della **struttura LVITEM.** Se in un'applicazione viene utilizzata la visualizzazione report, è necessario specificare il testo dell'elemento secondario.

L'esempio di codice C++ seguente riempie una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) e aggiunge gli elementi della visualizzazione elenco usando il messaggio [**\_ LVM INSERTITEM**](lvm-insertitem.md) o la macro [**corrispondente ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem). Poiché l'applicazione salva il proprio testo, specifica il valore LPSTR TEXTCALLBACK per il membro \_ **pszText** della **struttura LVITEM.** Se si specifica il valore LPSTR TEXTCALLBACK, il controllo invia un codice di notifica \_ [**\_ LVN GETDISPINFO**](lvn-getdispinfo.md) alla finestra proprietaria ogni volta che è necessario visualizzare un elemento.


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

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View controlli](list-view-controls-overview.md)
</dt> <dt>

[Uso di List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 




