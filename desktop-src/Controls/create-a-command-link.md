---
title: Come creare un collegamento di comando
description: In questo argomento viene descritto un modo per creare un collegamento di comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474462"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="acb7c-103">Come creare un collegamento di comando</span><span class="sxs-lookup"><span data-stu-id="acb7c-103">How to Create a Command Link</span></span>

<span data-ttu-id="acb7c-104">In questo argomento viene descritto un modo per creare un collegamento di comando.</span><span class="sxs-lookup"><span data-stu-id="acb7c-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="acb7c-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="acb7c-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="acb7c-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="acb7c-106">Technologies</span></span>

-   [<span data-ttu-id="acb7c-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="acb7c-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="acb7c-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="acb7c-108">Prerequisites</span></span>

-   <span data-ttu-id="acb7c-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="acb7c-109">C/C++</span></span>
-   <span data-ttu-id="acb7c-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="acb7c-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="acb7c-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="acb7c-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="acb7c-112">Passaggio 1: creare un'istanza del pulsante di collegamento al comando.</span><span class="sxs-lookup"><span data-stu-id="acb7c-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="acb7c-113">Nell'esempio di codice C++ riportato di seguito, la costante di stile [**BS \_ COMMANDLINK**](button-styles.md) specifica il pulsante come pulsante di collegamento del comando.</span><span class="sxs-lookup"><span data-stu-id="acb7c-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="acb7c-114">Passaggio 2: impostare l'etichetta del collegamento del comando e il testo della spiegazione</span><span class="sxs-lookup"><span data-stu-id="acb7c-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="acb7c-115">Utilizzare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per impostare l'etichetta del collegamento del comando e il testo supplementare rispettivamente tramite il messaggio [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e il messaggio di [**\_ Nota BCM**](bcm-setnote.md) .</span><span class="sxs-lookup"><span data-stu-id="acb7c-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="acb7c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="acb7c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acb7c-117">Informazioni sui pulsanti</span><span class="sxs-lookup"><span data-stu-id="acb7c-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="acb7c-118">Riferimento al controllo Button</span><span class="sxs-lookup"><span data-stu-id="acb7c-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="acb7c-119">Uso di pulsanti</span><span class="sxs-lookup"><span data-stu-id="acb7c-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="acb7c-120">Button</span><span class="sxs-lookup"><span data-stu-id="acb7c-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 