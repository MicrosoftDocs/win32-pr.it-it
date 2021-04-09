---
title: Come creare controlli Rich Edit
description: Per creare un controllo Rich Edit, chiamare la funzione CreateWindowEx, specificando la classe della finestra Rich Edit.
ms.assetid: E0F3E458-7907-42BD-841A-CB3D12628AA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6585e606cc77b307bf41aa938ed49e8baecb1349
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047412"
---
# <a name="how-to-create-rich-edit-controls"></a><span data-ttu-id="c6958-103">Come creare controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c6958-103">How to Create Rich Edit Controls</span></span>

<span data-ttu-id="c6958-104">Per creare un controllo Rich Edit, chiamare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando la classe della finestra Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c6958-104">To create a rich edit control, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the rich edit window class.</span></span> <span data-ttu-id="c6958-105">Per Microsoft Rich Edit 4,1 (Msftedit.dll), specificare \_ la classe MSFTEDIT come classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="c6958-105">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT\_CLASS as the window class.</span></span> <span data-ttu-id="c6958-106">Per tutte le versioni precedenti, specificare la classe RichEdit \_ .</span><span class="sxs-lookup"><span data-stu-id="c6958-106">For all previous versions, specify RICHEDIT\_CLASS.</span></span> <span data-ttu-id="c6958-107">Per ulteriori informazioni, vedere [versioni di Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c6958-107">For more information, see [Versions of Rich Edit](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="c6958-108">I controlli Rich Edit supportano la maggior parte degli stili della finestra utilizzati con i controlli di modifica e altri stili.</span><span class="sxs-lookup"><span data-stu-id="c6958-108">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="c6958-109">Se si desidera consentire più di una riga di testo nel controllo, è necessario specificare lo stile della finestra es su più [**\_ righe**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c6958-109">You should specify the [**ES\_MULTILINE**](edit-control-styles.md) window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="c6958-110">Per altre informazioni, vedere [stili del controllo Rich Edit](rich-edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c6958-110">For more information, see [Rich Edit Control Styles](rich-edit-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c6958-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c6958-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c6958-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c6958-112">Technologies</span></span>

-   [<span data-ttu-id="c6958-113">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c6958-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c6958-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c6958-114">Prerequisites</span></span>

-   <span data-ttu-id="c6958-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="c6958-115">C/C++</span></span>
-   <span data-ttu-id="c6958-116">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="c6958-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c6958-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c6958-117">Instructions</span></span>

### <a name="create-a-rich-edit-control"></a><span data-ttu-id="c6958-118">Creazione di un controllo Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c6958-118">Create a Rich Edit Control</span></span>

<span data-ttu-id="c6958-119">La funzione di esempio seguente crea un controllo Rich Edit e lo inizializza con un testo.</span><span class="sxs-lookup"><span data-stu-id="c6958-119">The following example function creates a rich edit control and initializes it with some text.</span></span>


```C++
HWND CreateRichEdit(HWND hwndOwner,        // Dialog box handle.
                    int x, int y,          // Location.
                    int width, int height, // Dimensions.
                    HINSTANCE hinst)       // Application or DLL instance.
{
    LoadLibrary(TEXT("Msftedit.dll"));
    
    HWND hwndEdit= CreateWindowEx(0, MSFTEDIT_CLASS, TEXT("Type here"),
        ES_MULTILINE | WS_VISIBLE | WS_CHILD | WS_BORDER | WS_TABSTOP, 
        x, y, width, height, 
        hwndOwner, NULL, hinst, NULL);
        
    return hwndEdit;
}
```



<span data-ttu-id="c6958-120">In Microsoft Visual Studio 2005 e versioni successive, è possibile aggiungere un controllo Rich Edit in un modello di finestra di dialogo trascinando il controllo dalla casella degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="c6958-120">In Microsoft Visual Studio 2005 and later, it is possible to add a rich edit control into a dialog template by dragging the control from the toolbox.</span></span> <span data-ttu-id="c6958-121">Tuttavia, l'operazione eseguita nell'editor finestre non garantisce che la libreria necessaria venga caricata prima della creazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="c6958-121">However, doing this in the dialog editor does not ensure that the required library will be loaded before the control is created.</span></span> <span data-ttu-id="c6958-122">È necessario chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Riched32.dll, Riched20.dll o Msftedit.dll prima della creazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c6958-122">It is necessary to call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Riched32.dll, Riched20.dll, or Msftedit.dll before the dialog is created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6958-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6958-123">Remarks</span></span>

<span data-ttu-id="c6958-124">Per usare gli stili di visualizzazione con questi controlli, un'applicazione deve includere un manifesto e deve chiamare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) all'inizio del programma.</span><span class="sxs-lookup"><span data-stu-id="c6958-124">To use visual styles with these controls, an application must include a manifest and must call the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function at the beginning of the program.</span></span> <span data-ttu-id="c6958-125">Per informazioni sugli stili di visualizzazione, vedere [stili di visualizzazione](themes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6958-125">For information on visual styles, see [Visual Styles](themes-overview.md).</span></span> <span data-ttu-id="c6958-126">Per informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c6958-126">For information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6958-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6958-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6958-128">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c6958-128">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="c6958-129">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c6958-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 