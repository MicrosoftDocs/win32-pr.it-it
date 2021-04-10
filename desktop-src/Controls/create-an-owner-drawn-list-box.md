---
title: Come creare una casella di riepilogo Owner-Drawn
description: In questo argomento viene illustrato come implementare una casella di riepilogo creata dal proprietario.
ms.assetid: AE6E8943-DC03-4A21-9F0A-9C70C6BD7481
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b48a56ca188fb2c277cc822dcb9a343205a331
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963596"
---
# <a name="how-to-create-an-owner-drawn-list-box"></a><span data-ttu-id="70711-103">Come creare una casella di riepilogo Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="70711-103">How to Create an Owner-Drawn List Box</span></span>

<span data-ttu-id="70711-104">In questo argomento viene illustrato come implementare una casella di riepilogo creata dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="70711-104">This topic demonstrates how to implement an owner-drawn list box.</span></span>

<span data-ttu-id="70711-105">Nell'esempio di codice C++ in questo argomento viene illustrato come creare una casella di riepilogo contenente cinque elementi creati dal proprietario: quattro implementazioni del disegno e un fork.</span><span class="sxs-lookup"><span data-stu-id="70711-105">The C++ code example in this topic shows how to draw a list box that contains five owner-drawn items: four drawing implements and a fork.</span></span> <span data-ttu-id="70711-106">Ogni elemento dell'elenco viene visualizzato come bitmap seguito dal nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="70711-106">Each list item appears as a bitmap followed by the name of the object.</span></span> <span data-ttu-id="70711-107">Un pulsante richiede all'utente di selezionare un elemento che non è simile a quello degli altri.</span><span class="sxs-lookup"><span data-stu-id="70711-107">A button prompts the user to select one item that is not like the others.</span></span> <span data-ttu-id="70711-108">Se si sceglie il pulsante con il fork selezionato, viene visualizzato il valore "Your are right!"</span><span class="sxs-lookup"><span data-stu-id="70711-108">Choosing the button with the fork selected displays a "You're right!"</span></span> <span data-ttu-id="70711-109">messaggio e chiude la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="70711-109">message and closes the dialog box.</span></span> <span data-ttu-id="70711-110">Se si sceglie il pulsante con qualsiasi altro elemento elenco selezionato, verrà visualizzato un messaggio di prova.</span><span class="sxs-lookup"><span data-stu-id="70711-110">Choosing the button with any other list item selected displays a "Try again!"</span></span> <span data-ttu-id="70711-111">il messaggio "Hello World!".</span><span class="sxs-lookup"><span data-stu-id="70711-111">message.</span></span>

<span data-ttu-id="70711-112">Nella casella di riepilogo sono presenti gli stili [**\_ HASSTRINGS**](list-box-styles.md) [**lbs \_ OwnerDrawFixed**](list-box-styles.md) e lbs, oltre agli stili standard della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="70711-112">The list box has the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) and [**LBS\_HASSTRINGS**](list-box-styles.md) styles, in addition to the standard list box styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="70711-113">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="70711-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="70711-114">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="70711-114">Technologies</span></span>

-   [<span data-ttu-id="70711-115">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="70711-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="70711-116">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="70711-116">Prerequisites</span></span>

-   <span data-ttu-id="70711-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="70711-117">C/C++</span></span>
-   <span data-ttu-id="70711-118">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="70711-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="70711-119">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="70711-119">Instructions</span></span>


<span data-ttu-id="70711-120">Per inizializzare una casella di riepilogo creata dal proprietario, l'applicazione deve caricare la stringa di testo e la bitmap associata per ogni elemento della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="70711-120">To initialize an owner-drawn list box, your application must load the text string and associated bitmap for each list box item.</span></span>

<span data-ttu-id="70711-121">Nell'esempio di codice C++ riportato di seguito, la routine della finestra di dialogo Inizializza la casella di riepilogo, ovvero l' **\_ elenco \_ IDC**, inviando il messaggio [**lb \_ ADDSTRING**](lb-addstring.md) per impostare il testo e quindi invia il messaggio [**lb \_ SETITEMDATA**](lb-setitemdata.md) per associare una bitmap a ogni elemento della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="70711-121">In the following C++ code example, the dialog box procedure initializes the list box, **IDC\_LIST\_STUFF**, by sending the [**LB\_ADDSTRING**](lb-addstring.md) message to set the text, and then sends the [**LB\_SETITEMDATA**](lb-setitemdata.md) message to associate a bitmap with each list box item.</span></span> <span data-ttu-id="70711-122">Il codice imposta inoltre l'altezza di ogni elemento della casella di riepilogo elaborando il messaggio [**WM \_ MeasureItem**](wm-measureitem.md) e disegna il testo e la bitmap per ogni elemento elaborando il messaggio [**WM \_ DrawItem**](wm-drawitem.md) .</span><span class="sxs-lookup"><span data-stu-id="70711-122">The code also sets the height of each list box item by processing the [**WM\_MEASUREITEM**](wm-measureitem.md) message and draws the text and bitmap for each item by processing the [**WM\_DRAWITEM**](wm-drawitem.md) message.</span></span>



```C++
#define XBITMAP 48 
#define YBITMAP 48 
 
#define BUFFER MAX_PATH 
 
HBITMAP hbmpPencil, hbmpCrayon, hbmpMarker, hbmpPen, hbmpFork; 
HBITMAP hbmpPicture, hbmpOld; 
 
void AddItem(HWND hwnd, PTSTR pstr, HBITMAP hbmp) 
{ 
    int lbItem; 
 
    lbItem = SendMessage(hwnd, LB_ADDSTRING, 0, (LPARAM)pstr); 
    SendMessage(hwnd, LB_SETITEMDATA, (WPARAM)lbItem, (LPARAM)hbmp); 
} 
 
INT_PTR CALLBACK DlgDrawProc(HWND hDlg, UINT message,
        UINT wParam, LONG lParam) 
{ 
    HWND hListBox; 
    PMEASUREITEMSTRUCT pmis; 
    PDRAWITEMSTRUCT pdis; 
    HDC hdcMem; 
       HBITMAP hbmp; 
    TCHAR achBuffer[BUFFER];
    size_t cch;
    int yPos; 
    int lbItem; 
    TEXTMETRIC tm; 
    RECT rcBitmap;
    HRESULT hr; 
    
    switch (message) 
    { 
         case WM_INITDIALOG: 
 
            // Load the bitmaps. g_hInst is the global HINSTANCE handle.
            hbmpPencil = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_PENCIL)); 
            hbmpCrayon = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CRAYON)); 
            hbmpMarker = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_MARKER)); 
            hbmpPen = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_PEN)); 
            hbmpFork = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_FORK)); 
 
            // Retrieve the list box handle. 
            hListBox = GetDlgItem(hDlg, IDC_LIST_STUFF); 
 
            // Initialize the list box text and associate a bitmap 
            // with each list box item. 
            AddItem(hListBox, L"pencil", hbmpPencil); 
            AddItem(hListBox, L"crayon", hbmpCrayon); 
            AddItem(hListBox, L"marker", hbmpMarker); 
            AddItem(hListBox, L"pen",    hbmpPen); 
            AddItem(hListBox, L"fork",   hbmpFork); 
 
            SetFocus(hListBox); 
            SendMessage(hListBox, LB_SETCURSEL, 0, 0); 
            return TRUE; 
 
        case WM_MEASUREITEM: 
 
            pmis = (PMEASUREITEMSTRUCT) lParam; 
 
            // Set the height of the list box items. 
            pmis->itemHeight = YBITMAP;

            return TRUE; 
 
        case WM_DRAWITEM: 
 
            pdis = (PDRAWITEMSTRUCT) lParam; 
 
            // If there are no list box items, skip this message. 
            if (pdis->itemID == -1) 
            { 
                break; 
            } 
 
            // Draw the bitmap and text for the list box item. Draw a 
            // rectangle around the bitmap if it is selected. 
            switch (pdis->itemAction) 
            { 
                case ODA_SELECT: 
                case ODA_DRAWENTIRE: 
 
                    // Draw the bitmap associated with the item. 
                    //
                    // Get the item bitmap.
                    hbmpPicture = (HBITMAP)SendMessage(pdis->hwndItem, 
                        LB_GETITEMDATA, pdis->itemID, 0); 
 
                    // Create a compatible device context. 
                    hdcMem = CreateCompatibleDC(pdis->hDC); 

                    // Select the item bitmap into the compatible device
                    // context and save the old bitmap.
                    hbmpOld = (HBITMAP) SelectObject(hdcMem, hbmpPicture); 
 
                    // Copy the bitmap into the compatible device context.
                    BitBlt(pdis->hDC, 
                        pdis->rcItem.left, pdis->rcItem.top, 
                        pdis->rcItem.right - pdis->rcItem.left, 
                        pdis->rcItem.bottom - pdis->rcItem.top, 
                        hdcMem, 0, 0, SRCCOPY); 
 
                    // Draw the string associated with the item. 
                    //
                    // Get the item string from the list box.
                    SendMessage(pdis->hwndItem, LB_GETTEXT, 
                        pdis->itemID, (LPARAM)achBuffer); 
 
                    // Get the metrics for the current font.
                    GetTextMetrics(pdis->hDC, &tm); 

                    // Calculate the vertical position for the item string 
                    // so that the string will be vertically centered in the 
                    // item rectangle.
                    yPos = (pdis->rcItem.bottom + pdis->rcItem.top - 
                        tm.tmHeight) / 2;
                        
                    // Get the character length of the item string.
                    hr = StringCchLength(achBuffer, BUFFER, &cch);
                    if (FAILED(hr))
                    {
                        // TODO: Handle error.
                    }
 
                    // Draw the string in the item rectangle, leaving a six
                    // pixel gap between the item bitmap and the string.
                    TextOut(pdis->hDC, XBITMAP + 6, yPos, achBuffer, cch);                         
 
                    // Clean up.
                    SelectObject(hdcMem, hbmpOld); 
                    DeleteDC(hdcMem); 
 
                    // Is the item selected? 
                    if (pdis->itemState & ODS_SELECTED) 
                    { 
                        // Set RECT coordinates to surround only the 
                        // bitmap. 
                        rcBitmap.left = pdis->rcItem.left; 
                        rcBitmap.top = pdis->rcItem.top; 
                        rcBitmap.right = pdis->rcItem.left + XBITMAP; 
                        rcBitmap.bottom = pdis->rcItem.top + YBITMAP; 
 
                        // Draw a rectangle around bitmap to indicate 
                        // the selection. 
                        DrawFocusRect(pdis->hDC, &rcBitmap); 
                    } 
                    break; 
 
                case ODA_FOCUS: 
 
                    // Do not process focus changes. The focus caret 
                    // (outline rectangle) indicates the selection. 
                    // The IDOK button indicates the final 
                    // selection. 
                    break; 
            } 
            return TRUE; 
 
        case WM_COMMAND: 
 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    // Get the selected item's text. 
                    lbItem = SendMessage(GetDlgItem(hDlg, IDC_LIST_STUFF), 
                        LB_GETCURSEL, 0, 0); 

                    // Get the selected item's bitmap. 
                    hbmp = (HBITMAP) SendMessage(GetDlgItem(hDlg, IDC_LIST_STUFF), 
                         LB_GETITEMDATA, lbItem, 0); 
 
                    // If the item is not the correct answer, tell the 
                    // user to try again. 
                    //
                    // If the item is the correct answer, congratulate 
                    // the user and destroy the dialog box. 
                    if (hbmp != hbmpFork) 
                    { 
                        MessageBox(hDlg, L"Try again!", L"Oops", MB_OK); 
                        return FALSE; 
                    } 
                    else 
                    { 
                        MessageBox(hDlg, L"You're right!", 
                            L"Congratulations.", MB_OK); 
 
                      // Fall through. 
                    } 
 
                case IDCANCEL: 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
 
                default: 
 
                    return FALSE; 
            } 
 
        case WM_DESTROY: 
 
            // Free the bitmap resources. 
            DeleteObject(hbmpPencil); 
            DeleteObject(hbmpCrayon); 
            DeleteObject(hbmpMarker); 
            DeleteObject(hbmpPen); 
            DeleteObject(hbmpFork); 
 
            return TRUE; 
 
        default: 
            return FALSE; 
 
    } 
    return FALSE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="70711-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70711-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70711-124">Riferimento al controllo casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="70711-124">List Box Control Reference</span></span>](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[<span data-ttu-id="70711-125">Informazioni sulle caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="70711-125">About List Boxes</span></span>](about-list-boxes.md)
</dt> <dt>

[<span data-ttu-id="70711-126">Uso di caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="70711-126">Using List Boxes</span></span>](using-list-boxes.md)
</dt> </dl>

 

 




