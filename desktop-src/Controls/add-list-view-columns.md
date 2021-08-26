---
title: Come aggiungere List-View colonne
description: Questo argomento illustra come aggiungere colonne a un controllo visualizzazione elenco.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee71065729502410d189493527af0e3e37663a4a2aaf541852454af7fa4a5aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922081"
---
# <a name="how-to-add-list-view-columns"></a>Come aggiungere List-View colonne

Questo argomento illustra come aggiungere colonne a un controllo visualizzazione elenco. Le colonne vengono usate per visualizzare gli elementi e gli elementi secondari quando un controllo visualizzazione elenco si trova nella visualizzazione report (dettagli). Il testo delle colonne selezionate può essere visualizzato anche nella visualizzazione affiancata.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per aggiungere una colonna a un controllo visualizzazione elenco, inviare il messaggio [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) o usare la macro [**\_ ListView InsertColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) Per eliminare una colonna, usare il [**messaggio LVM \_ DELETECOLUMN.**](lvm-deletecolumn.md)

Nell'esempio di codice C++ seguente viene chiamata la macro [**\_ ListView InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) per aggiungere colonne a un controllo visualizzazione elenco. Le intestazioni di colonna sono definite nel file di intestazione dell'applicazione come risorse stringa, numerate consecutivamente a partire da IDS \_ FIRSTCOLUMN. Il numero di colonne è definito nel file di intestazione come **C \_ COLUMNS**.


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

[Informazioni di riferimento sul controllo List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni List-View controllo](list-view-controls-overview.md)
</dt> <dt>

[Uso dei List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

 




