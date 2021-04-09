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
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="52695-103">Come aggiungere List-View colonne</span><span class="sxs-lookup"><span data-stu-id="52695-103">How to Add List-View Columns</span></span>

<span data-ttu-id="52695-104">In questo argomento viene illustrato come aggiungere colonne a un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="52695-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="52695-105">Le colonne vengono utilizzate per visualizzare gli elementi e gli elementi secondari quando un controllo visualizzazione elenco è nella visualizzazione report (Dettagli).</span><span class="sxs-lookup"><span data-stu-id="52695-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="52695-106">Il testo delle colonne selezionate può essere visualizzato anche nella visualizzazione affiancata.</span><span class="sxs-lookup"><span data-stu-id="52695-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="52695-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="52695-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="52695-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="52695-108">Technologies</span></span>

-   [<span data-ttu-id="52695-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="52695-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="52695-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="52695-110">Prerequisites</span></span>

-   <span data-ttu-id="52695-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="52695-111">C/C++</span></span>
-   <span data-ttu-id="52695-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="52695-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="52695-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="52695-113">Instructions</span></span>


<span data-ttu-id="52695-114">Per aggiungere una colonna a un controllo visualizzazione elenco, inviare il messaggio [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) o usare la macro [**\_ INSERTCOLUMN di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="52695-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="52695-115">Per eliminare una colonna, usare il messaggio [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="52695-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="52695-116">Nell'esempio di codice C++ riportato di seguito viene chiamata la macro [**\_ InsertColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) per aggiungere colonne a un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="52695-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="52695-117">Le intestazioni di colonna vengono definite nel file di intestazione dell'applicazione come risorse di stringa, numerate consecutivamente iniziando con ID \_ FIRSTCOLUMN.</span><span class="sxs-lookup"><span data-stu-id="52695-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="52695-118">Il numero di colonne è definito nel file di intestazione come **\_ colonne C**.</span><span class="sxs-lookup"><span data-stu-id="52695-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="52695-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52695-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52695-120">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="52695-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="52695-121">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="52695-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="52695-122">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="52695-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




