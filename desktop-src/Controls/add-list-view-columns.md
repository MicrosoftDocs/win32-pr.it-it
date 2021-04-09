---
title: Come aggiungere List-View colonne
description: In questo argomento viene illustrato come aggiungere colonne a un controllo visualizzazione elenco.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047613"
---
# <a name="how-to-add-list-view-columns"></a>Come aggiungere List-View colonne

In questo argomento viene illustrato come aggiungere colonne a un controllo visualizzazione elenco. Le colonne vengono utilizzate per visualizzare gli elementi e gli elementi secondari quando un controllo visualizzazione elenco è nella visualizzazione report (Dettagli). Il testo delle colonne selezionate può essere visualizzato anche nella visualizzazione affiancata.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per aggiungere una colonna a un controllo visualizzazione elenco, inviare il messaggio [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) o usare la macro [**\_ INSERTCOLUMN di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) . Per eliminare una colonna, usare il messaggio [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

Nell'esempio di codice C++ riportato di seguito viene chiamata la macro [**\_ InsertColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) per aggiungere colonne a un controllo visualizzazione elenco. Le intestazioni di colonna vengono definite nel file di intestazione dell'applicazione come risorse di stringa, numerate consecutivamente iniziando con ID \_ FIRSTCOLUMN. Il numero di colonne è definito nel file di intestazione come **\_ colonne C**.


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
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

 

 




