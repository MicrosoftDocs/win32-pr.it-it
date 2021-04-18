---
title: Come creare una finestra delle proprietà
description: Nell'esempio riportato in questa sezione viene creata una finestra delle proprietà che contiene due pagine \ 8212, una per l'impostazione delle proprietà del tipo di carattere di una cella in un foglio di calcolo e un'altra per l'impostazione delle proprietà del bordo della cella.
ms.assetid: 61ACF87A-938C-4487-ACEB-484FCB677C6A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15abd44f3a583afd99c5d943b9105c8734b73c1
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323816"
---
# <a name="how-to-create-a-property-sheet"></a><span data-ttu-id="aa539-103">Come creare una finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="aa539-103">How to Create a Property Sheet</span></span>

<span data-ttu-id="aa539-104">Nell'esempio riportato in questa sezione viene creata una finestra delle proprietà che contiene due pagine, una per l'impostazione delle proprietà del tipo di carattere di una cella in un foglio di calcolo e un'altra per l'impostazione delle proprietà del bordo della cella.</span><span class="sxs-lookup"><span data-stu-id="aa539-104">The example in this section creates a property sheet that contains two pages—one for setting the font properties of a cell in a spreadsheet, and another for setting the border properties of the cell.</span></span>

<span data-ttu-id="aa539-105">Nell'esempio vengono definite le pagine compilando una coppia di strutture [**PROPSHEETPAGE**](pss-propsheetpage.md) e specificando l'indirizzo nella struttura [**PROPSHEETHEADER**](pss-propsheetheader.md) che viene passato alla funzione [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .</span><span class="sxs-lookup"><span data-stu-id="aa539-105">The example defines the pages by filling a pair of [**PROPSHEETPAGE**](pss-propsheetpage.md) structures and specifying the address in the [**PROPSHEETHEADER**](pss-propsheetheader.md) structure that is passed to the [**PropertySheet**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="aa539-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="aa539-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="aa539-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="aa539-107">Technologies</span></span>

-   [<span data-ttu-id="aa539-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="aa539-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="aa539-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="aa539-109">Prerequisites</span></span>

-   <span data-ttu-id="aa539-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="aa539-110">C/C++</span></span>
-   <span data-ttu-id="aa539-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="aa539-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="aa539-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="aa539-112">Instructions</span></span>

### <a name="create-a-property-sheet"></a><span data-ttu-id="aa539-113">Crea una finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="aa539-113">Create a Property Sheet</span></span>

<span data-ttu-id="aa539-114">Nell'esempio di codice riportato di seguito viene illustrato come creare una finestra delle proprietà a due pagine.</span><span class="sxs-lookup"><span data-stu-id="aa539-114">The following code example demonstrates how to create a two–page property sheet.</span></span>


```C++
// DoPropertySheet - creates a property sheet that contains two pages.
//
// hwndOwner - handle to the owner window of the property sheet.
//
// Global variables
//     g_hinst - instance handle

extern HINSTANCE g_hinst;

VOID DoPropertySheet(HWND hwndOwner)
{
    PROPSHEETPAGE psp[2];
    
    PROPSHEETHEADER psh;
    
    psp[0].dwSize      = sizeof(PROPSHEETPAGE);
    psp[0].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[0].hInstance   = g_hinst;
    psp[0].pszTemplate = MAKEINTRESOURCE(DLG_FONT);
    psp[0].pszIcon     = MAKEINTRESOURCE(IDI_FONT);
    psp[0].pfnDlgProc  = FontDialogProc;
    psp[0].pszTitle    = MAKEINTRESOURCE(IDS_FONT)
    psp[0].lParam      = 0;
    psp[0].pfnCallback = NULL;
    psp[1].dwSize      = sizeof(PROPSHEETPAGE);
    psp[1].dwFlags     = PSP_USEICONID | PSP_USETITLE;
    psp[1].hInstance   = g_hinst;
    psp[1].pszTemplate = MAKEINTRESOURCE(DLG_BORDER);
    psp[1].pszIcon     = MAKEINTRESOURCE(IDI_BORDER);
    psp[1].pfnDlgProc  = BorderDialogProc;
    psp[1].pszTitle    = MAKEINTRESOURCE(IDS_BORDER);
    psp[1].lParam      = 0;
    psp[1].pfnCallback = NULL;
    
    psh.dwSize      = sizeof(PROPSHEETHEADER);
    psh.dwFlags     = PSH_USEICONID | PSH_PROPSHEETPAGE;
    psh.hwndParent  = hwndOwner;
    psh.hInstance   = g_hinst;
    psh.pszIcon     = MAKEINTRESOURCE(IDI_CELL_PROPERTIES);
    psh.pszCaption  = (LPSTR) "Cell Properties";
    psh.nPages      = sizeof(psp) / sizeof(PROPSHEETPAGE);
    psh.nStartPage  = 0;
    psh.ppsp        = (LPCPROPSHEETPAGE) &psp;
    psh.pfnCallback = NULL;
    
    PropertySheet(&psh);
    
    return;
}
```



## <a name="remarks"></a><span data-ttu-id="aa539-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa539-115">Remarks</span></span>

<span data-ttu-id="aa539-116">I modelli, le icone e le etichette della finestra di dialogo per le pagine vengono caricati dalle risorse contenute nel file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aa539-116">The dialog box templates, icons, and labels for the pages are loaded from the resources contained in the application's executable file.</span></span> <span data-ttu-id="aa539-117">Anche l'icona per la finestra delle proprietà viene caricata dalle risorse dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aa539-117">The icon for the property sheet is also loaded from the application's resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa539-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa539-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa539-119">Utilizzo delle finestre delle proprietà</span><span class="sxs-lookup"><span data-stu-id="aa539-119">Using Property Sheets</span></span>](using-property-sheets.md)
</dt> <dt>

[<span data-ttu-id="aa539-120">Esempio di proprietà</span><span class="sxs-lookup"><span data-stu-id="aa539-120">Property sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/property)
</dt> </dl>

 

 




