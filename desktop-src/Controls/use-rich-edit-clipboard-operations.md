---
title: Come utilizzare le operazioni Rich Edit Clipboard
description: Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963505"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a><span data-ttu-id="3393c-103">Come utilizzare le operazioni Rich Edit Clipboard</span><span class="sxs-lookup"><span data-stu-id="3393c-103">How to Use Rich Edit Clipboard Operations</span></span>

<span data-ttu-id="3393c-104">Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico.</span><span class="sxs-lookup"><span data-stu-id="3393c-104">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="3393c-105">È inoltre possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3393c-105">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3393c-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="3393c-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3393c-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="3393c-107">Technologies</span></span>

-   [<span data-ttu-id="3393c-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="3393c-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3393c-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="3393c-109">Prerequisites</span></span>

-   <span data-ttu-id="3393c-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="3393c-110">C/C++</span></span>
-   <span data-ttu-id="3393c-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="3393c-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3393c-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="3393c-112">Instructions</span></span>

### <a name="use-a-rich-edit-clipboard-operation"></a><span data-ttu-id="3393c-113">Usa un'operazione Rich Edit Clipboard</span><span class="sxs-lookup"><span data-stu-id="3393c-113">Use a Rich Edit Clipboard Operation</span></span>

<span data-ttu-id="3393c-114">Come con un controllo di modifica, è possibile copiare o tagliare il contenuto della selezione corrente usando il messaggio [**WM \_ Copy**](/windows/desktop/dataxchg/wm-copy) o [**WM \_ Cut**](/windows/desktop/dataxchg/wm-cut) .</span><span class="sxs-lookup"><span data-stu-id="3393c-114">As with an edit control, you can copy or cut the contents of the current selection by using the [**WM\_COPY**](/windows/desktop/dataxchg/wm-copy) or [**WM\_CUT**](/windows/desktop/dataxchg/wm-cut) message.</span></span> <span data-ttu-id="3393c-115">Analogamente, è possibile incollare il contenuto degli Appunti in un controllo Rich Edit usando il messaggio [**WM \_ paste**](/windows/desktop/dataxchg/wm-paste) .</span><span class="sxs-lookup"><span data-stu-id="3393c-115">Similarly, you can paste the contents of the clipboard into a rich edit control by using the [**WM\_PASTE**](/windows/desktop/dataxchg/wm-paste) message.</span></span> <span data-ttu-id="3393c-116">Il controllo incolla il primo formato disponibile che riconosce, che presumibilmente è il formato più descrittivo.</span><span class="sxs-lookup"><span data-stu-id="3393c-116">The control pastes the first available format that it recognizes, which presumably is the most descriptive format.</span></span>

<span data-ttu-id="3393c-117">Per incollare un formato degli Appunti specifico, è possibile usare il messaggio [**\_ PASTESPECIAL em**](em-pastespecial.md) .</span><span class="sxs-lookup"><span data-stu-id="3393c-117">To paste a specific clipboard format, you can use the [**EM\_PASTESPECIAL**](em-pastespecial.md) message.</span></span> <span data-ttu-id="3393c-118">Questo messaggio è utile per le applicazioni con un comando **Incolla speciale** che consente all'utente di selezionare il formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="3393c-118">This message is useful for applications with a **Paste Special** command that enables the user to select the clipboard format.</span></span> <span data-ttu-id="3393c-119">È possibile usare il [**messaggio \_ CANPASTE em**](em-canpaste.md) per determinare se un formato specificato è riconosciuto dal controllo.</span><span class="sxs-lookup"><span data-stu-id="3393c-119">You can use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether a given format is recognized by the control.</span></span>

<span data-ttu-id="3393c-120">È anche possibile usare il [**messaggio \_ CANPASTE em**](em-canpaste.md) per determinare se un formato degli Appunti disponibile viene riconosciuto da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="3393c-120">You can also use the [**EM\_CANPASTE**](em-canpaste.md) message to determine whether any available clipboard format is recognized by a rich edit control.</span></span> <span data-ttu-id="3393c-121">Questo messaggio è utile quando si elabora il messaggio [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) .</span><span class="sxs-lookup"><span data-stu-id="3393c-121">This message is useful when processing the [**WM\_INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) message.</span></span> <span data-ttu-id="3393c-122">Un'applicazione potrebbe abilitare o rendere grigio il comando **Incolla** a seconda che il controllo possa incollare qualsiasi formato disponibile.</span><span class="sxs-lookup"><span data-stu-id="3393c-122">An application might enable or gray its **Paste** command depending on whether the control can paste any available format.</span></span>

<span data-ttu-id="3393c-123">I controlli Rich Edit registrano due formati degli Appunti:</span><span class="sxs-lookup"><span data-stu-id="3393c-123">Rich edit controls register two clipboard formats:</span></span>

-   <span data-ttu-id="3393c-124">Formato RTF</span><span class="sxs-lookup"><span data-stu-id="3393c-124">Rich Text Format</span></span>
-   <span data-ttu-id="3393c-125">Formato RTF senza oggetti</span><span class="sxs-lookup"><span data-stu-id="3393c-125">Rich Text Format Without Objects</span></span>
-   <span data-ttu-id="3393c-126">Testo RichEdit e oggetti</span><span class="sxs-lookup"><span data-stu-id="3393c-126">RichEdit Text and Objects</span></span>

<span data-ttu-id="3393c-127">Un'applicazione può registrare questi formati usando la funzione [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , specificando i \_ valori CF RTF, CF \_ RTFNOOBJS e CF \_ RETEXTOBJ.</span><span class="sxs-lookup"><span data-stu-id="3393c-127">An application can register these formats by using the [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) function, specifying the CF\_RTF, CF\_RTFNOOBJS, and CF\_RETEXTOBJ values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3393c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3393c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3393c-129">Uso di controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="3393c-129">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="3393c-130">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="3393c-130">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 