---
title: Come creare un pulsante
description: Per creare pulsanti in modo dinamico, usare la funzione CreateWindow o CreateWindowEx. In questo argomento viene illustrato come utilizzare la funzione CreateWindow per creare un pulsante di push predefinito.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047624"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="98d04-104">Come creare un pulsante</span><span class="sxs-lookup"><span data-stu-id="98d04-104">How to Create a Button</span></span>

<span data-ttu-id="98d04-105">Per creare pulsanti in modo dinamico, usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="98d04-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="98d04-106">In questo argomento viene illustrato come utilizzare la funzione **CreateWindow** per creare un pulsante di push predefinito.</span><span class="sxs-lookup"><span data-stu-id="98d04-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="98d04-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="98d04-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="98d04-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="98d04-108">Technologies</span></span>

-   [<span data-ttu-id="98d04-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="98d04-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="98d04-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="98d04-110">Prerequisites</span></span>

-   <span data-ttu-id="98d04-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="98d04-111">C/C++</span></span>
-   <span data-ttu-id="98d04-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="98d04-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="98d04-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="98d04-113">Instructions</span></span>


<span data-ttu-id="98d04-114">Usare la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) per creare un controllo Button.</span><span class="sxs-lookup"><span data-stu-id="98d04-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="98d04-115">Nel seguente esempio di C++, il *parametro \_ HWND m* è l'handle per la finestra padre.</span><span class="sxs-lookup"><span data-stu-id="98d04-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="98d04-116">Lo stile [**BS \_ DEFPUSHBUTTON**](button-styles.md) specifica che deve essere creato un pulsante di push predefinito.</span><span class="sxs-lookup"><span data-stu-id="98d04-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="98d04-117">Si noti che è necessario specificare i valori delle dimensioni e della posizione perché l'uso di **CW \_ usedefault (** per un pulsante Imposta i valori su zero.</span><span class="sxs-lookup"><span data-stu-id="98d04-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="98d04-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98d04-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98d04-119">Informazioni sui pulsanti</span><span class="sxs-lookup"><span data-stu-id="98d04-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="98d04-120">Riferimento al controllo Button</span><span class="sxs-lookup"><span data-stu-id="98d04-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="98d04-121">Uso di pulsanti</span><span class="sxs-lookup"><span data-stu-id="98d04-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="98d04-122">Button</span><span class="sxs-lookup"><span data-stu-id="98d04-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 