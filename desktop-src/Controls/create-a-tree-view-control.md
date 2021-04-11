---
title: Come creare un controllo Tree-View
description: Per creare un controllo di visualizzazione albero, usare la funzione CreateWindowEx, specificando il \_ valore di TreeView del WC per la classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118542"
---
# <a name="how-to-create-a-tree-view-control"></a>Come creare un controllo Tree-View

Per creare un controllo di visualizzazione albero, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando il valore di [**\_ TreeView del WC**](common-control-window-classes.md) per la classe Window. La classe della finestra visualizzazione albero viene registrata nello spazio degli indirizzi dell'applicazione quando viene caricata la DLL del controllo comune. Per assicurarsi che la DLL venga caricata, utilizzare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-an-instance-of-a-tree-view-control"></a>Creare un'istanza di un controllo Tree-View

Nell'esempio seguente viene creato un controllo di visualizzazione albero che viene ridimensionato per adattarsi all'area client della finestra padre. USA anche funzioni definite dall'applicazione per associare un elenco di immagini al controllo e aggiungere elementi al controllo.


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a>Commenti

Quando si crea un controllo di visualizzazione struttura ad albero, è possibile inviare anche un messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) per impostare il tipo di carattere da utilizzare per il testo. È necessario inviare questo messaggio prima di inserire elementi. Per impostazione predefinita, una visualizzazione albero utilizza il carattere del titolo dell'icona. Anche se è possibile personalizzare il tipo di carattere per elemento utilizzando [disegno personalizzato](custom-draw.md), il controllo di visualizzazione albero utilizza le dimensioni del tipo di carattere specificato dal messaggio **WM \_ sefont** per determinare la spaziatura e il layout.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Tree-View](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 